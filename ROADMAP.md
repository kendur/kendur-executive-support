# Roadmap

This roadmap reflects current priorities for the **Executive Support System** *(working title)*. It will evolve as the project matures.

---

## Phase 0 — Foundation *(current)*

**Goal:** Establish the documentation and architectural foundation before any application code is written.

- [x] Repository created
- [x] README — problem, philosophy, status, AI stance
- [x] Vision document
- [x] Project charter
- [x] Architecture principles
- [x] Capture ingestion design
- [x] Product tier definitions
- [x] CONTRIBUTING, AI_USAGE, SECURITY, CHANGELOG
- [x] GitHub issue templates and pull request template
- [ ] First Architecture Decision Records (ADRs) for key early choices
- [ ] Research notes on comparable systems
- [ ] Glossary of project-specific terms

---

## Phase 1 — Notion Prototype

**Goal:** A working, manual Notion workspace that implements the core capture-to-action workflow without any automation.

- [ ] Define Notion database schema (Inbox, Actions, Projects, Reference, Archive)
- [ ] Define Personal and Work profile structures
- [ ] Build and document the manual triage workflow
- [ ] Define source and provenance tagging convention
- [ ] Document the unified view pattern (Personal + Work in a single dashboard)
- [ ] Test and refine with real daily use
- [ ] Publish a Notion template (community edition)

---

## Phase 2 — Automation Adapters

**Goal:** Add automation for common capture sources as optional, replaceable adapters.

- [ ] Define the adapter interface contract
- [ ] n8n adapter (self-hosted option)
- [ ] Zapier adapter
- [ ] Make (Integromat) adapter
- [ ] Tasker adapter (Android, mobile capture)
- [ ] Email-to-inbox adapter
- [ ] Document how to connect a voice recorder (PLAUD, Omi, Fieldy, phone recorder, or any transcript source)
- [ ] Pocket / read-later integration
- [ ] Manual file upload workflow (transcripts, PDFs)

---

## Phase 3 — AI Enhancement Layer

**Goal:** Add AI-assisted processing as an optional layer on top of the working manual system.

- [ ] Define AI enhancement interface (provider-agnostic)
- [ ] Transcript summarisation and action extraction
- [ ] Suggested routing (Inbox → Project or Action)
- [ ] Restart cue generation
- [ ] Weekly review assistant
- [ ] Document how to connect any compatible LLM or AI service

---

## Phase 4 — Product and Community

**Goal:** Formalise the community edition and define any paid tier.

- [ ] Finalise license for code (community edition)
- [ ] Finalise license for content and documentation
- [ ] Publish community Notion template
- [ ] Define paid tier features (see [docs/product-tiers.md](docs/product-tiers.md))
- [ ] Set up community discussion space
- [ ] Contribution guidelines mature enough for external contributors

---

## Future Considerations

- Integration with the broader **Nexus** personal operating system (working title)
- Native mobile capture companion
- Self-hosted backend option
- Multi-user household or small-team support

---

*Items in this roadmap may change. This is a public project developed by a single maintainer with community input.*
