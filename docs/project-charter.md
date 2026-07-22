# Project Charter

## Project Name

**Executive Support System** *(working title)*

---

## Problem Statement

People who manage high volumes of information across Personal and Work profiles lack a reliable, low-friction
system for turning captured information into clear next actions. Existing tools either require too much upfront
structure, conflate capture with triage, or lock users into a single platform or methodology.

---

## Goal

Build a Notion-centered, capture-source-agnostic system that:

1. Allows fast, incomplete-tolerant capture from any source
2. Preserves profile, source provenance, and restart cues for every item
3. Provides a clear, manual triage workflow that works without AI or automation
4. Supports AI and automation as optional, provider-agnostic enhancement layers
5. Maintains Personal and Work profiles separately while allowing a unified view
6. Can evolve into a monetised product while maintaining a free community edition

---

## Scope

### In Scope

- Documentation of the system design, principles, and workflows
- A Notion workspace template implementing the core workflow
- Optional automation adapters for common capture sources
- Optional AI enhancement integrations (provider-agnostic)
- An optional provider-agnostic AI Guide Pack for setup and ongoing assistance
- A community edition available to anyone
- Hosted automation, optional managed intelligence/support, and later Platform/Enterprise tracks
- A future first-party backend if it improves reliability or replaces third-party automation adapters

### Out of Scope

- A custom-built application during the documentation phase
- Team or multi-user collaboration features (single-person system)
- Real-time communication tools (the system integrates with them but does not replace them)
- Diagnostic, treatment, or therapeutic claims of any kind

---

## Non-Goals

- Replacing email, calendar, or chat tools
- Automating decision-making
- Becoming a general-purpose project management tool
- Requiring any specific AI provider, automation platform, or recording device

---

## Intended Users

Primary: A single person managing obligations across Personal and Work profiles, receiving information from
multiple sources, who wants a system they can trust without being locked into a vendor or methodology.

Secondary: Anyone who finds parts of the system useful and wants to adapt or fork them.

---

## Constraints

- **No employer names.** Personal and Work are the default public profile labels.
- **No AI required.** The core workflow must function without any AI or automation.
- **No vendor lock-in.** Notion, automation tools, and AI providers are all replaceable adapters.
- **No production code in the documentation phase.** This phase produces only documents and design artefacts.
- **No tutorial dependency for the core workflow.** The base template must be understandable without tutorials or reference docs.
- **Planned license split.** Pending final review, template/content material will use CC BY 4.0 and software will use Apache 2.0.
- **Clinical boundary.** The project makes no diagnostic, treatment, or therapeutic claims.
- **Working title.** "Executive Support System" may change. "Nexus" is also a working title.

---

## Success Criteria

- Phase 0: A complete documentation foundation, including history and ADRs, that can guide prototype development
- Phase 1: A working Notion prototype used daily by the primary maintainer and understandable without tutorials or reference docs
- Phase 2: At least one automation adapter published and tested
- Phase 3: At least one AI enhancement integration documented and working
- Phase 4: A published community template and a defined paid tier

---

## Stakeholders

| Role | Description |
|---|---|
| Primary maintainer | Owner and lead decision-maker |
| Community contributors | Provide feedback, improvements, and optional implementations |
| Community users | Use the published templates and adapters |
| Future customers | Users of any paid tier |

---

## Governance

This is a single-maintainer project developed in public. All decisions rest with the primary maintainer. Community input is welcomed through issues and pull requests. See [CONTRIBUTING.md](../CONTRIBUTING.md).

---

## Related Documents

- [docs/vision.md](vision.md) — why this project exists
- [docs/history-and-timeline.md](history-and-timeline.md) — project origin and timeline
- [docs/architecture-principles.md](architecture-principles.md) — structural decisions
- [docs/capture-ingestion.md](capture-ingestion.md) — how information enters the system
- [docs/product-tiers.md](product-tiers.md) — community and paid tier definitions
- [ROADMAP.md](../ROADMAP.md) — delivery phases
