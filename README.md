# Executive Support System *(working title)*

> A Notion-centered, capture-source-agnostic system for turning thoughts, conversations, meetings, and obligations into clear next actions.

---

## The Problem

Information arrives from everywhere—voice notes, phone calls, meeting transcripts, emails, passing ideas, and half-formed obligations. Most productivity tools ask you to organize before you think. The result: either a perfectly maintained system nobody actually uses, or an overflowing inbox that creates guilt instead of clarity.

The Executive Support System takes the opposite approach: **capture first, structure later, act always.**

---

## Philosophy

- **Capture must be fast and tolerate incomplete thoughts.** A half-formed idea captured is always better than a perfect idea forgotten.
- **Context is not optional.** Every item preserves its source (how it arrived), provenance (where it came from), and enough of a restart cue to re-engage without re-reading everything.
- **The core works without AI.** Automation and AI are enhancement layers—useful when available, never required.
- **Personal and Work live separately.** The two profiles are maintained independently but can surface together in a unified view when needed.
- **Flat beats nested.** Avoid deep task hierarchies. One level of project context is usually enough.
- **Intuitive without tutorials.** Workflows a user can understand on first contact are preferred over powerful workflows that require documentation to follow.
- **Notion is the primary interface.** Everything else—automation tools, capture devices, AI providers—are adapters.

---

## What This Is (and Isn't)

| This system is… | This system is not… |
|---|---|
| A thinking and triage layer | A replacement for your calendar or email |
| A way to surface forgotten commitments | A task tracker with enforced methodology |
| A bridge between messy capture and clean action | A medical or wellness tool |
| Designed for one person at the centre of many obligations | A team project management tool |

---

## Intended Users

This system is built for people who:

- Move between Personal and Work contexts frequently
- Receive information across many sources (voice, text, meetings, email)
- Struggle with "I'll deal with that later" accumulation
- Want to own their system rather than depend on a single vendor
- Are comfortable building and adapting tools to their own needs

---

## Current Status

This repository is in the **documentation and architecture phase**. No production application code exists yet. The documents here define the problem, the principles, and the intended structure.

See [ROADMAP.md](ROADMAP.md) for what comes next.

---

## AI-Optional Design

AI can summarise transcripts, suggest next actions, and route captured items—but none of those things are required for the system to function. The manual workflow comes first. AI and automation are layered on top.

No specific AI provider, LLM, or service is assumed or required. See [AI_USAGE.md](AI_USAGE.md) for details on how AI is used in this project (including in development).

---

## The Nexus Vision

This project is one layer of a larger personal operating system called **Nexus** (also a working title). Nexus aims to unify how a person captures, reflects on, and acts on information across every area of their life. The Executive Support System is the action-and-obligation layer of that vision.

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

No license has been assigned yet. The project will use separate licenses for code and content. Until a license is published, all rights are reserved by the repository owner.
