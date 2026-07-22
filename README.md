# Executive Support System *(working title)*

> A Notion-centered, capture-source-agnostic system for turning raw capture into clear next actions.

---

## The Problem

Information arrives from everywhere—raw audio, files, transcripts, emails, manual notes, and half-formed
obligations. Most productivity tools ask you to organise before you think. The result: either a perfectly
maintained system nobody actually uses, or an overflowing inbox that creates guilt instead of clarity.

The Executive Support System takes the opposite approach: **capture first, structure later, act always.**

---

## Philosophy

- **Capture must be fast and tolerate incomplete thoughts.** A half-formed idea captured is always better than a perfect idea forgotten.
- **Profiles are explicit.** Personal and Work are the default top-level profiles. Context is reserved for the
  situational detail needed to resume a task.
- **The core works without AI.** Automation and AI are enhancement layers—useful when available, never required.
- **Personal and Work live separately.** The two profiles are maintained independently but can surface together
  in a unified view when needed.
- **Flat beats nested.** Avoid deep task hierarchies. One level of project context is usually enough.
- **Intuitive without tutorials.** The core template should be understandable on first contact without tutorials
  or reference docs.
- **Notion is the primary interface.** Everything else—automation tools, capture devices, AI providers—are adapters.

---

## What This Is (and Isn't)

| This system is… | This system is not… |
|---|---|
| A thinking and triage layer | A replacement for your calendar or email |
| A way to surface forgotten commitments | A task tracker with enforced methodology |
| A bridge between messy capture and clean action | A source of diagnostic, treatment, or therapeutic claims |
| Designed for one person at the centre of many obligations | A team project management tool |

---

## Intended Users

This system is built for people who:

- Move between Personal and Work profiles frequently
- Receive information across many sources (audio, files, transcripts, meetings, email, manual entry)
- Struggle with "I'll deal with that later" accumulation
- Want to own their system rather than depend on a single vendor

---

## Current Status

This repository is in the **documentation and architecture phase**. No production application code exists yet. The documents here define the problem, the principles, and the intended structure.

See [ROADMAP.md](ROADMAP.md) for what comes next.

The planned Community edition remains free, openly licensed, forkable, and updated in public while maintained.
Any paid path is intended to build on hosted automation and optional managed support rather than gate the core
workflow. See [docs/product-tiers.md](docs/product-tiers.md).

---

## AI-Optional Design

AI can summarise transcripts, suggest next actions, and route captured items—but none of those things are required for the system to function. The manual workflow comes first. AI and automation are layered on top.

No specific AI provider, LLM, or service is assumed or required. See [AI_USAGE.md](AI_USAGE.md) for details on how AI is used in this project (including in development).

An optional provider-agnostic AI Guide Pack may later help people set up and use AI assistance at their own
skill level, but the core template must remain understandable without it.

---

## The Nexus Vision

This project is one layer of a larger personal operating system called **Nexus** (also a working title). Nexus aims to unify how a person captures, reflects on, and acts on information across every area of their life. The Executive Support System is the action-and-obligation layer of that vision.

See [docs/history-and-timeline.md](docs/history-and-timeline.md) for the project origin and foundational decisions.

---

## Repository Structure

```
/
├── README.md                        ← you are here
├── ROADMAP.md                       ← what comes next
├── CONTRIBUTING.md                  ← how to contribute
├── AI_USAGE.md                      ← AI policy and disclosure
├── SECURITY.md                      ← security policy
├── CHANGELOG.md                     ← version history
└── docs/
    ├── vision.md                    ← why this project exists
    ├── history-and-timeline.md      ← origin, timeline, and governance context
    ├── project-charter.md           ← scope, goals, constraints
    ├── architecture-principles.md   ← structural decisions
    ├── capture-ingestion.md         ← how information enters the system
    ├── product-tiers.md             ← community vs. paid tiers
    ├── research/                    ← background research and references
    └── decisions/                   ← Architecture Decision Records (ADRs)
```

---

## Public Development

This project is developed in public. Issues, discussions, and pull requests are welcome. Contributions are governed by [CONTRIBUTING.md](CONTRIBUTING.md).

AI-assisted development is permitted and used. Human maintainers are responsible for all accepted work. See [AI_USAGE.md](AI_USAGE.md).

---

## License

The planned license split, pending final review, is **CC BY 4.0** for template/content material and
**Apache 2.0** for software. Until licenses are formally published, all rights remain reserved by the
repository owner.
