# Executive Support System *(working title)*

> A Notion-centered, capture-source-agnostic system for turning thoughts, conversations, meetings, and obligations into clear next actions.

## The problem

Information arrives faster than people can organize it. Most productivity tools ask users to classify, schedule, and structure an item at the moment it appears. That creates friction exactly when memory and attention are most fragile.

This system takes the opposite approach: **capture first, clarify later, act with context.**

## Core principles

- **Capture incomplete thoughts quickly.** A fragment saved is more useful than a complete idea forgotten.
- **Preserve context and restart cues.** Users should be able to return without reconstructing the whole task.
- **Work without AI.** Automation and AI are optional enhancement layers.
- **Use Personal and Work profiles.** They remain separate and may appear together in a unified view.
- **Prefer flat, visible structure.** Deep task nesting is avoided.
- **Require no tutorial for core use.** Capture, clarification, Today planning, and completion must be understandable from the interface itself.
- **Keep adapters replaceable.** Recorders, automation platforms, calendars, and AI providers connect through documented contracts.
- **Keep Notion primary.** Notion is the initial interface and operational workspace; external services extend it.

## Intended users

This system is designed for people who:

- receive information from many sources;
- lose thoughts or context quickly;
- move between Personal and Work responsibilities;
- want a trusted system without adopting a rigid methodology;
- may have little technical experience;
- want the option to add automation or AI without being required to do so.

## See the system at work

The [founder thought-stream before-and-after example](docs/examples/founder-thought-stream-before-and-after.md) preserves a real, unedited audio transcript beside an example of AI-assisted processing. It shows how the system can extract intent, prioritize decisions, retain unfinished threads, and identify a next action without discarding the original thought.

## Product model

The complete manual community system is intended to remain free and openly licensed. Users may duplicate, modify, fork, and redistribute it under the published attribution terms.

Future paid offerings may provide hosted automation, managed connectors, optional intelligence, migration help, monitoring, and support. Paid services sell reduced setup and maintenance burden rather than access to the core workflow.

See [docs/product-tiers.md](docs/product-tiers.md).

## AI-optional design

AI may summarize, extract possible actions, suggest routing, create restart cues, and help users configure the system. The manual workflow remains complete without it.

The planned **AI Guide Pack** is a provider-agnostic set of prompts, reference material, progressive onboarding questions, and tests that can help a user set up and operate the template at their current skill level. See [docs/ai-guide-pack.md](docs/ai-guide-pack.md).

## Relationship to Nexus

This project is the first bounded, testable, and potentially monetizable module on the path toward **Nexus**, a broader personal operating-system concept. It must succeed as a standalone product while preserving clear integration points for later Nexus modules.

## Current status

The repository is in the documentation, research, and architecture phase. The next major deliverable is a manual Notion prototype tested through real daily use.

See [ROADMAP.md](ROADMAP.md).

## Repository structure

```text
README.md
ROADMAP.md
AI_USAGE.md
SECURITY.md
CHANGELOG.md
docs/
  vision.md
  project-charter.md
  architecture-principles.md
  capture-ingestion.md
  ai-guide-pack.md
  product-tiers.md
  examples/
  history/
  research/
  decisions/
```

## Public development

The project is developed in public. AI-assisted development is permitted and disclosed; human maintainers remain accountable for accepted work.

## Licensing status

No license files have been added yet. The planned split, pending final review, is:

- **CC BY 4.0** for the Notion template, prompts, documentation, diagrams, and research;
- **Apache License 2.0** for code, connectors, scripts, and backend services;
- a separate branding policy to distinguish official tested releases from community forks.

Until those files are published, all rights remain reserved.