# ADR-0002: Personal and Work Profiles

**Date:** 2026-07-22  
**Status:** Accepted

## Context

The first design user needs personal and employer-related tasks to remain separate while still being visible in one planning surface. Public terminology must remain portable.

## Decision

Use **Profile** as the top-level public separation field, with default values **Personal** and **Work**. Employer names remain private user configuration.

## Alternatives considered

- One mixed task database without a profile field.
- Employer-specific public fields.
- Completely isolated systems with no unified view.

## Consequences

- Public examples and prompts use Personal and Work.
- Records may be filtered separately or surfaced together.
- Situational task context remains a separate concept from Profile.