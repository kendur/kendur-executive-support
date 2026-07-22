# Architecture Principles

These principles remain stable while implementations change.

## 1. Notion is the primary interface

Notion provides the initial database, view layer, and main interaction surface. Other tools extend it through documented contracts.

## 2. The core workflow is manual and complete

Capture, clarification, planning, review, recovery, and completion must work without automation or AI. Every enhanced workflow needs a usable manual path.

## 3. Capture, clarification, and action are separate states

Capture must be fast and incomplete-tolerant. Clarification determines meaning and next action. Action presents enough context to begin or resume.

## 4. Context and provenance are first-class data

Every meaningful record should preserve:

- source;
- origin or related event;
- raw capture where available;
- supporting files or links;
- last completed step;
- restart cue.

## 5. Personal and Work are profiles

**Profile** is the public top-level separation concept. Personal and Work records remain logically separate and may be shown together through a unified view.

Situational context—such as location, device, energy, or available time—is separate from Profile.

## 6. Flat hierarchy is preferred

Use Profile → Project → Action as the normal structure. Checklists, dependencies, and milestones are preferred to deep subtask trees.

## 7. Core workflows require no tutorial

A new user should understand where to capture, what needs clarification, what to do now, what is blocked, and how to complete an item from the interface itself.

Advanced documentation may explain customization and integrations. It must not be required for ordinary use.

## 8. Complexity stays behind the interface

Relations, formulas, automation, and AI may be technically complex. The user-facing decision at any moment should remain small, explicit, and reversible where practical.

## 9. Adapters are replaceable

Capture sources, calendars, automation platforms, storage systems, and AI providers connect through defined inputs and outputs. Provider-specific behavior belongs inside adapters.

## 10. Notion-native, backend-portable

Use native Notion capabilities where they provide a reliable experience. Near-term automation may use n8n, Zapier, Make, Tasker, or similar tools. Workflow contracts must allow those services to be replaced later by a first-party backend without redesigning the Notion schema or user experience.

## 11. AI is optional and provider-agnostic

AI capabilities are defined by function—such as summarize, extract actions, suggest a next action, or create a restart cue—rather than by vendor. Users may choose no AI, a hosted provider, a local model, or a future managed service.

## 12. AI autonomy is graduated

Suggestions are the default. Routine, reversible actions may be automated when the user explicitly enables them. Consequential, destructive, conflicting, or external actions require approval.

## 13. The system must recover gracefully

A missed review or neglected backlog must not make the system unusable. Recovery views should prioritize current commitments, stale ambiguity, and intentional dropping rather than demanding complete repair.

## 14. The system must reduce obligation

If maintaining the system creates as much work as it saves, the design has failed. Every property, workflow, notification, and integration must justify its maintenance cost.

## 15. No lock-in at any layer

- Notion data must remain exportable.
- Workflows are documented before vendor-specific implementation.
- AI providers can be changed without losing core data.
- The community template works without a paid add-on.
- Official tested releases remain distinguishable from forks.

Specific accepted decisions are recorded in [docs/decisions/](decisions/).