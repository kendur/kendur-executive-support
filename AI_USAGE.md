# AI Usage Policy

This document describes how artificial intelligence tools are used in the **Executive Support System** project—both in development of the project itself and in the design of the system being built.

---

## AI Use in Project Development

AI-assisted development is permitted and used in this project. This includes:

- Drafting and editing documentation
- Generating code snippets, templates, and configuration examples
- Reviewing and suggesting improvements to text or structure
- Brainstorming approaches to design problems

**Human responsibility is non-negotiable.** All content accepted into this repository has been reviewed and approved by a human maintainer. AI output is treated as a draft, not a final product. Factual accuracy, appropriateness, and quality are the responsibility of the maintainer who accepts the work.

Contributors who use AI assistance in preparing their contributions should disclose this in their pull request description.

---

## AI as a System Feature

The Executive Support System is designed to work fully without AI. The core workflow—capture, triage, action—is manual. AI is an optional enhancement layer.

When AI is used within the system, it operates in the following roles:

| Role | Description |
|---|---|
| Summariser | Condenses transcripts, notes, or captured text into shorter, structured form |
| Action extractor | Identifies potential next actions from unstructured content |
| Router | Suggests how to categorise or assign captured items |
| Restart cue generator | Produces a short context summary to help re-engage with an item after a gap |
| Review assistant | Supports periodic reviews by surfacing patterns or forgotten items |

None of these roles are required. Each can be performed manually.

---

## Provider Agnosticism

No specific AI provider, LLM, or AI service is assumed, required, or endorsed by this project.

The system is designed so that any compatible AI service can be connected as an adapter. Provider-specific integrations are documented as optional adapters, not core components.

---

## What AI Will Not Do in This System

- AI will not make decisions on behalf of the user.
- AI will not modify or delete captured items without explicit user action.
- AI will not be given access to data that the user has not explicitly shared with it.
- AI output will always be presented as a suggestion, not a conclusion.

---

## Disclosure Log

Significant use of AI tools in producing project documentation or design artefacts will be noted here as the project evolves.

| Date | Description |
|---|---|
| *(none yet)* | |

---

*This policy may be updated as the project matures and as AI tooling evolves.*
