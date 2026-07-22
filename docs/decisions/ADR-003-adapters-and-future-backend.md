# ADR-003: Capture-source-agnostic adapters and future first-party backend

**Date:** 2026-07-22
**Status:** Accepted

## Context

The system must accept information from many sources today without permanently binding itself to current
third-party automation tools.

## Options Considered

- Optimise for one capture source and one automation platform
- Accept many capture sources through replaceable adapters
- Delay adapter design until a custom backend exists

## Decision

Treat capture as source-agnostic and define adapters around a shared Inbox contract. n8n, Zapier, Make, and
similar tools are valid interim implementations, and a future first-party backend may replace them.

## Reasoning

This allows the system to work with current tools while preserving a path to a more cohesive first-party
implementation later.

## Consequences

Public documentation should describe the contract and supported source types, not assume one provider. Profile
labels remain Personal and Work, while context refers only to situational task detail.
