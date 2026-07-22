# ADR-001: Notion-first manual core

**Date:** 2026-07-22
**Status:** Accepted

## Context

The project needs a core workflow that remains usable before any custom software or optional integrations are
built.

## Options Considered

- Build a custom application first
- Use Notion as the primary interface with a manual-first workflow
- Depend on automation and AI from the start

## Decision

Use Notion as the primary interface and keep the core workflow manual first.

## Reasoning

This keeps the first usable version simple, testable in daily use, and independent of any single automation or
AI provider.

## Consequences

Automation and AI remain optional layers. A future first-party backend is still allowed, but it must support
the same core workflow rather than replace it conceptually.
