# Platform regression rehearsal: n8n recovery and Notion assignees

Prepared: 2026-11-09
Status: test plan prepared; live tests NOT RUN.
Scope: the executive-support module's optional automation adapters. This is a rehearsal proposal, not a deployment record or a change to the product's accepted architecture.

## Current evidence and limits

- This repository's README describes a documentation/prototype phase with no application code. The canonical capture contract is in [capture-ingestion.md](../capture-ingestion.md); [architecture principles](../architecture-principles.md) require a complete manual workflow and optional AI.
- KenDur.Cloud's [n8n service record](https://github.com/kendur/KenDur.Cloud/blob/a0655b1cd8907d7f7f52e725f881383debe1f0bb/docs/services/n8n.md) documents a September 18 deployment of 2.39.8 with PostgreSQL 17.9. This is historical repository evidence, NOT verification of the current running version.
- Its [deployment](https://github.com/kendur/KenDur.Cloud/blob/a0655b1cd8907d7f7f52e725f881383debe1f0bb/infra/vps/n8n/compose.yaml) uses a tag supplied through the environment, persistent volumes with fixed names, a disabled public API, and external networks. Do not reuse that definition unchanged for an isolated rehearsal.
- No live host session, Docker runtime, isolated staging endpoint, or dedicated Notion test page/connection was available during preparation. No service was upgraded and no agent was assigned.
- Current n8n version, production workflow inventory, paid Notion plan, test-agent access, and remaining credits are unverified.

## Upstream changes being tested

1. [n8n 2.46.7 release, November 9](https://github.com/n8n-io/n8n/releases/tag/n8n%402.46.7) is stable/latest. [Implementation rationale](https://github.com/n8n-io/n8n/pull/42862): paused/queued execution loading could repeatedly exhaust memory before execution state changed. Loading attempts are now counted; repeated failures terminate as crashed. Overlapping wait resumes are avoided and queued startup recovery loads executions individually.
2. [Notion changelog, November 9](https://developers.notion.com/page/changelog): Custom Agents can be assigned through people properties, may start a run, and appear in reads as bot users. Avatar URLs can be null. Agent-interaction capability and explicit Agent access are required. [People-property reference](https://developers.notion.com/reference/page-property-values#people) explains bot user IDs and notes that List all users omits Custom Agents.
3. [Custom Agent requirements](https://www.notion.com/help/custom-agents): Business or Enterprise. Agent data access is separately configured. Ordinary capture must not depend on agent availability, subscription, or credits.

No upstream migration deadline is stated for either change.

## Isolation and setup

Use synthetic captures with stable capture_id values, Personal/Work profiles, source references, and harmless text. Evidence must exclude credentials, actual captures, webhook secrets, and personal information.

For n8n:

- Record the actual running image tag/digest and database version read-only before choosing the baseline. Target 2.46.7 explicitly, not a floating latest tag.
- Use a disposable Docker host or isolated staging project, new encryption key and database credentials, separate named volumes, loopback-only port, and a private network. Do not attach production networks or mount production volumes.
- Use synthetic workflows and a local test sink. Do not import active production workflows, credentials, notification destinations, or external triggers. A restored database can activate workflows and send real messages.
- Apply a container memory limit; run the deliberate exhaustion case only on a disposable host where losing the container cannot affect other services.
- Observe recovery from outside the n8n process. The instance being tested cannot reliably report its own crash.
- Before a later production upgrade, use the existing backup/restore procedure and verify that a full restore can decrypt a test credential. Database migrations require restoring the pre-upgrade database for rollback; changing the image tag alone is not a rollback.

For Notion:

- Use a dedicated test database, a named people property, two synthetic pages, a human test assignee, and a harmless Custom Agent with access only to those test resources.
- Disable external tools, outbound messages, and unrelated triggers on the test agent. Preassign it manually to a seed page to obtain its bot user ID.
- Pin the integration's current Notion-Version and record capabilities and Agent access selection. Do not expand access to the whole workspace.
- Enable agent assignment only for the explicit agent test. Set a small available agent credit limit and record usage before/after; stop on unexpected repeated runs. Do not record tokens.

## n8n cases

| ID | Procedure | Pass condition |
|---|---|---|
| N1 | Send one synthetic capture through a Wait workflow. Restart while waiting; allow its due time to pass. | One downstream completion for that capture_id; provenance and profile survive. |
| N2 | Queue several synthetic captures under constrained concurrency, restart with work pending, then drain. | Every capture is accounted for once at the sink; failed items remain visible and recoverable. Record execution mode; this is not evidence for Redis queue mode unless tested separately. |
| N3 | In disposable staging only, persist a synthetic payload large enough that loading it on resume exceeds the container limit. Restart and observe subsequent recovery attempts. | Service exits the repeated-crash cycle; the offending execution becomes crashed; a new small capture still completes. Record actual attempts and timings rather than guessing from restart count. |
| N4 | Observe due waiting work whose loading overlaps the scheduler's next check. | No simultaneous duplicate resume of the same execution. Sink count and logs agree. If this condition cannot be reproduced, mark NOT RUN rather than infer success from N1. |
| N5 | Detect the N3 failure externally, reconcile its capture_id, and recover through the documented manual path. | One actionable alert/recovery entry, no silent loss, and no duplicate final record. Healthz alone is not sufficient evidence. |
| N6 | Rehearse restore on the disposable project using its pre-upgrade snapshot, original test encryption key, and prior image. | Synthetic data and test credential are usable; no connection to production destinations occurs. |

N2 tests startup recovery of queued executions. If Nexus later uses Redis-backed queue mode, add a distinct worker/restart/cancellation rehearsal; this plan does not claim that coverage.

## Notion cases

| ID | Procedure | Pass condition |
|---|---|---|
| P1 | Read a test page containing a human and an assigned Custom Agent. Exercise adapter parsing with a null bot avatar and omitted optional user details. | Preserve every user ID and type without requiring email, name, or avatar; no bot is dropped. No new assignment write is needed for this read test. |
| P2 | Change an unrelated property, then deliberately round-trip the complete people property on the test page. | Original human and bot memberships survive. Record whether the explicit people write starts a run. |
| P3 | With agent-interaction capability removed, and separately with Agent access removed, attempt an agent assignment. | Assignment is denied; existing assignees remain unchanged; the capture stays available for manual handling. Record actual error codes. |
| P4 | Explicitly enable delegation and assign the harmless agent once. | The intended agent runs only within test resources; capture is preserved; run/credit evidence is recorded. Assignment success is not proof that agent work completed. |
| P5 | Simulate a lost response after assignment and repeat the proposed retry path under a bounded budget. | Determine whether reassignment retriggers work. Do not assume idempotency. Automatic retry remains disabled if a duplicate run cannot be excluded or reconciled. |
| P6 | Disable delegation and test without agent access or available AI capacity. | Manual capture, clarification, and human assignment still work. An unknown agent result stays pending for reconciliation rather than being blindly retried. |

List all users is not an agent directory. A rich-text user mention is not a substitute for a people-property assignment. Do not silently grant agent access when a write fails.

## Evidence and decision

For each case record: UTC timestamp, operator, version/digest or Notion-Version, sanitized fixture ID, prerequisites, steps, observed result, expected result, execution/run IDs, credits before/after when relevant, and PASS/FAIL/NOT RUN. Keep sensitive evidence in private operator storage; publish only sanitized summaries here.

Current results:

| Cases | Result | Missing requirement |
|---|---|---|
| N1-N6 | NOT RUN | Disposable Docker staging and verified deployment baseline |
| P1-P6 | NOT RUN | Dedicated Notion test resources, connection capability and test-agent access |

Release decision remains pending:

- n8n: require successful recovery, reconciliation, independent failure visibility, and restore evidence before proposing a live upgrade.
- Notion: require assignee preservation and denied-access coverage before adapter adoption. Keep optional delegation off until run accounting, retry behavior, and bounded access pass.
- Failing or unavailable AI must not block capture. No new provider, plan purchase, production deployment, or architectural authority change is approved by this test plan.

AI assistance: Codex inspected repository documents and prepared this plan. No live test results were generated.
