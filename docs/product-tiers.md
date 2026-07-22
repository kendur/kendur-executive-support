# Product Tiers

This document defines the intended product structure for the Executive Support System.

---

## Guiding Principle

The core system remains available as a free Community edition. Revenue, if introduced, comes from hosted
automation, support, or other value-added services rather than gating the fundamental workflow.

---

## Community edition

The Community edition is intended to be:

- Free to use
- Openly licensed
- Forkable
- Updated publicly for the lifetime of the project while it is actively maintained

As components become available, the Community edition is the public baseline for documentation, templates,
manual workflows, adapter specifications, and accepted ADRs.

The core template must be understandable without tutorials or reference docs. An optional provider-agnostic
AI Guide Pack may later help with setup and ongoing assistance at different user skill levels, but it is not
required to use the core system.

---

## Derivatives and official status

Derivatives are permitted under the published licenses, but they must preserve attribution and link back to
the canonical source repository.

Forkable does not mean official. Project branding, "official" status, and any claim that a release is tested
or maintainer-supported remain distinct and may be reserved for first-party releases.

---

## Service path beyond Community

Any paid offering should extend the Community edition rather than replace it. Likely paths include:

- Hosted automation for people who do not want to self-run n8n, Zapier, Make, or equivalent tooling
- Optional managed intelligence/support, including onboarding or ongoing help
- Later Platform or Enterprise tracks if the architecture justifies them

A first-party backend remains in scope as a future replacement for third-party automation tools if that
improves reliability, portability, or product coherence.

---

## Planned licensing

Pending final review, the planned split is:

- **CC BY 4.0** for template and content material
- **Apache 2.0** for software

Until those licenses are formally published, all rights remain reserved by the repository owner.
