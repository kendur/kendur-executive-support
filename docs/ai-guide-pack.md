# AI Guide Pack

## Purpose

The AI Guide Pack helps a user set up, understand, and maintain the Executive Support System without requiring the project maintainer to teach each user personally.

It is optional. The core template remains usable without AI.

## Package structure

The Guide Pack should contain versioned, provider-agnostic artifacts:

1. **Core role prompt** — purpose, boundaries, terminology, and expected behavior.
2. **Template reference** — databases, properties, views, workflow states, and supported actions.
3. **Progressive onboarding** — a few questions at a time, asked only when the answer is needed.
4. **User capability profile** — technical comfort, preferred explanation depth, connected tools, and desired autonomy.
5. **Capability prompts** — setup, troubleshooting, capture clarification, integration guidance, and review assistance.
6. **Tests** — example inputs and expected safe behavior.
7. **Update reference** — canonical project URL, version, compatibility notes, and migration guidance.

## Onboarding rule

Do not begin with a long questionnaire. Ask the minimum needed for the next useful step, then learn through actual use.

Example opening questions:

1. Do you want the manual system only, or help connecting automation or AI?
2. Are you comfortable editing Notion databases and properties?
3. Which capture sources do you want to use first?

Additional questions should appear only when relevant.

## Skill adaptation

The guide should adapt its instructions:

- **Guided:** one step at a time with confirmation.
- **Standard:** concise instructions with brief explanations.
- **Technical:** schemas, APIs, automation logic, and implementation details.

The user may change mode at any time.

## Provider behavior

The Guide Pack may be used with Notion AI, ChatGPT, Claude, compatible local models, or future providers. It must state which functions require browsing, file access, Notion access, or external tools and offer a manual alternative when those capabilities are unavailable.

## Authority

The guide may explain, propose, draft, and troubleshoot. Routine reversible actions may be performed only when the user explicitly authorizes them and the connected tool supports them. Consequential, destructive, or external actions require confirmation.

## Update model

The installed prompt should identify:

- Guide Pack version;
- template version;
- canonical source URL;
- supported schema range;
- date last checked for updates.

An AI may tell the user that updates exist, but it must not silently replace the user's customized system.