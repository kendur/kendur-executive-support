# Architecture Principles

These principles guide structural and design decisions for the Executive Support System. They are intended to be stable even as implementations change.

---

## 1. Notion is the primary interface, not the only component

Notion serves as the database, view layer, and primary interaction surface. Other tools—automation platforms, AI services, capture devices—are adapters that feed into or extend Notion. If Notion were replaced with another platform, the principles here should still apply.

**Implication:** Never design a workflow that requires a non-Notion tool. Design workflows that work in Notion first, then add adapters.

---

## 2. The core workflow is manual

The system must function without automation or AI. Every automated step must have a documented manual equivalent. This ensures the system never breaks because a service is unavailable, changes its pricing, or is discontinued.

**Implication:** Automation and AI integrations are documented as optional enhancements, not core requirements.

---

## 3. Capture is separate from triage, which is separate from action

These three activities happen at different times and in different mental states. The architecture must accommodate them independently.

- Capture happens fast, with minimal friction, and tolerates incomplete or unstructured input
- Triage happens deliberately, with enough context to decide what something is
- Action happens with enough restart information to engage without re-reading everything

**Implication:** The Inbox is the capture zone. Triage moves items out of the Inbox. Actions are never in the Inbox.

---

## 4. Profile, source provenance, and restart cues are first-class data

Every captured item should record:

- **Profile** — whether it belongs to Personal, Work, or another explicitly defined profile
- **Source** — how it arrived (voice note, email, meeting, manual entry, etc.)
- **Provenance** — where it came from (which meeting, which person, which project)
- **Restart cue** — enough context to re-engage without reading everything (a short summary, a key question,
  or the last decision made)

Situational context remains useful, but it is distinct from the top-level Personal/Work profile choice.

**Implication:** The Notion schema must include fields for profile, source, provenance, and restart cues.
These are not optional.

---

## 5. Personal and Work are the default top-level profiles

Items, projects, and actions are tagged as Personal or Work. The two profiles do not need to share databases,
though they can appear together in a unified view.

**Implication:** Design for two parallel workspaces or clearly separated sections within one workspace. Never
mix unlabelled items.

---

## 6. Flat hierarchy is preferred

Avoid deep nesting of projects, tasks, or pages. One level of project context above an action is usually sufficient. Deep nesting creates navigation debt and orphaned items.

**Implication:** Limit nesting to: Profile (Personal/Work) → Project → Action. Sub-tasks are acceptable but
not sub-sub-tasks.

---

## 7. Adapters are replaceable

Any tool used for automation (n8n, Zapier, Make, Tasker) or AI (any LLM or AI service) must be replaceable
without redesigning the core system. The interface between the adapter and Notion is the contract; the
adapter itself is an implementation detail.

A first-party backend remains an allowed future implementation if it becomes the best way to satisfy the same
contract.

**Implication:** Document the expected input and output format for each integration point. Do not hard-code assumptions about a specific provider.

---

## 8. Workflows must be intuitive without tutorials

A new user should be able to pick up the core capture-triage-action loop from the Notion workspace itself, without reading documentation. Documentation exists to explain the why and the deeper options, not the basic how.

**Implication:** Naming, layout, and structure within Notion should be self-explanatory. Avoid clever names or non-obvious conventions.

---

## 9. The system should not become a source of additional obligation

If maintaining the system creates as much work as the problems it solves, it has failed. Regular reviews of friction points and workflow burden are part of system maintenance.

**Implication:** Prefer simpler designs even at the cost of some capability. Complexity that the user never engages with is waste.

---

## 10. No lock-in at any layer

- Notion data should be exportable
- Automation workflows should be documented in a platform-agnostic way before implementation
- AI integrations should be designed to switch providers without data loss
- The Notion template should be importable without requiring any paid add-on

**Implication:** Document workflows in plain language before implementing them in any specific tool.

---

## Decisions

Specific architectural decisions are recorded as Architecture Decision Records (ADRs) in [docs/decisions/](decisions/).
