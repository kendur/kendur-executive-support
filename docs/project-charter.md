# Project Charter

## Project name

**Executive Support System** *(working title)*

## Purpose

Build a Notion-centered knowledge, task-management, and scheduling system that reduces the effort required to remember, clarify, start, resume, schedule, and complete work.

The primary maintainer is the first design user and private pilot. The architecture must also be capable of becoming a useful open community product and a sustainable paid service.

## Problem statement

Many people can understand what needs to be done and still struggle to convert intention into action. Relevant friction includes rapid idea loss, working-memory pressure, vague obligations, task-initiation difficulty, time blindness, interruption, and loss of context.

The system must support these problems as a productivity and information-management tool. It makes no diagnostic, treatment, or therapeutic claims.

## Goals

1. Capture incomplete thoughts from text, audio, transcripts, email, files, meetings, and future sources.
2. Preserve source provenance, supporting context, and restart cues.
3. Provide a complete manual workflow without AI or automation.
4. Make core workflows understandable without tutorials or reference documents.
5. Use default Personal and Work profiles that remain separate and may appear in a unified view.
6. Keep capture, automation, and AI providers replaceable.
7. Produce a free, openly licensed community edition.
8. Support future paid services for hosting, automation, intelligence, migration, monitoring, and support.
9. Preserve interfaces for later integration into Nexus.

## Scope

### In scope

- behavioral and interaction-design research;
- a Notion workspace template;
- manual capture, clarification, planning, review, recovery, and completion workflows;
- optional capture adapters;
- optional deterministic automation;
- an optional provider-agnostic AI Guide Pack;
- Personal and Work profile handling;
- open community distribution;
- a future first-party backend that may replace n8n, Zapier, Make, or similar services;
- product validation and paid-service design.

### Outside the first release

- team collaboration;
- multi-tenant SaaS infrastructure;
- billing and enterprise administration;
- a complete custom application;
- autonomous consequential decision-making;
- migration of every historical record;
- diagnostic, treatment, or therapeutic functionality.

A future custom backend remains in scope as an implementation path. It is deferred rather than prohibited.

## Intended users

The core system must support users with little technical experience. Advanced users may connect their own automation platform, AI provider, local model, recorder, or custom integration.

A user should be able to complete the ordinary capture-to-done workflow without learning Notion database mechanics.

## Product profiles

**Profile** is the public top-level separation concept.

Default profiles:

- Personal
- Work

Employer names belong only in private user configuration and must not appear in public examples, screenshots, prompts, or marketing.

## Constraints

- Notion is the initial primary interface.
- The complete core workflow works without AI.
- AI and automation are optional and provider-agnostic.
- Core workflows require no tutorial.
- Deep task nesting is avoided.
- Public examples use Personal and Work profiles.
- Community forks remain distinct from official tested releases.
- Product claims remain supported by evidence and avoid clinical promises.

## Success criteria

- A thought can be captured in under ten seconds.
- A new user can capture, clarify, plan Today, and complete an item without outside instructions.
- Personal and Work records can be viewed together and separately.
- Tasks retain their purpose, source, context, and restart cue.
- Due dates and scheduled work remain separate.
- Interrupted work can be resumed without reconstructing the whole project.
- AI can be disabled or changed without redesigning the core system.
- External automation can later move to a first-party backend without redesigning the Notion experience.
- The system remains usable after several days of neglect.
- Maintenance requires less effort than the system saves.

## Governance

The project is developed publicly under a single primary maintainer. Community input is welcome. Agents and contributors may propose plans and draft changes; the maintainer retains final approval over consequential decisions.

## Related documents

- [Vision](vision.md)
- [Architecture principles](architecture-principles.md)
- [Capture and ingestion](capture-ingestion.md)
- [AI Guide Pack](ai-guide-pack.md)
- [Product tiers](product-tiers.md)
- [Project history](history/0001-origin-and-context.md)
- [Roadmap](../ROADMAP.md)