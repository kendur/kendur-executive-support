# ADR-0001: Notion-Centered, AI-Optional Core

**Date:** 2026-07-22  
**Status:** Accepted

## Context

The system needs to provide immediate value through a familiar visual workspace while allowing automation and intelligence to grow later.

## Decision

Notion is the initial primary interface and operational workspace. The complete core workflow must remain usable without AI or external automation.

## Alternatives considered

- Build a custom application first.
- Require an AI agent for core operation.
- Use several disconnected task and knowledge tools.

## Consequences

- Manual workflows are designed and tested first.
- AI and automation remain optional adapters.
- A future backend may replace third-party automation without redesigning the user-facing Notion system.