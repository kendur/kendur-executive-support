# Architecture Decision Records

This folder contains Architecture Decision Records (ADRs) for the Executive Support System.

---

## What Is an ADR?

An Architecture Decision Record documents a significant decision made about the structure, design, or direction of the system. Each ADR captures:

- The context in which the decision was made
- The options that were considered
- The decision that was made
- The reasoning behind it
- The consequences of the decision

ADRs are immutable once accepted. If a decision changes, a new ADR is created that supersedes the old one. This preserves the history of why decisions were made.

---

## ADR Template

When creating a new ADR, use this structure:

```markdown
# ADR-NNN: [Short Title]

**Date:** YYYY-MM-DD
**Status:** Proposed | Accepted | Superseded by ADR-NNN

## Context

[What is the situation or problem that requires a decision?]

## Options Considered

- Option A: [description]
- Option B: [description]
- Option C: [description]

## Decision

[What was decided?]

## Reasoning

[Why was this decision made over the alternatives?]

## Consequences

[What are the trade-offs or downstream effects of this decision?]
```

---

## Proposing a New ADR

Open a pull request with the new ADR file named `ADR-NNN-short-title.md` where NNN is the next sequential number. See [CONTRIBUTING.md](../../CONTRIBUTING.md).

---

## Current ADRs

- [ADR-001: Notion-first manual core](ADR-001-notion-first-manual-core.md)
- [ADR-002: Open community edition with service-based paid path](ADR-002-open-community-and-service-path.md)
- [ADR-003: Capture-source-agnostic adapters and future first-party backend](ADR-003-adapters-and-future-backend.md)
