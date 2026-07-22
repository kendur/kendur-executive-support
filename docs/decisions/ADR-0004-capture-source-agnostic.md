# ADR-0004: Capture-Source-Agnostic Design

**Date:** 2026-07-22  
**Status:** Accepted

## Context

Capture hardware and transcription services evolve quickly. Building a complete recorder ecosystem first would delay the product, while depending on one vendor would create lock-in.

## Decision

Vendors may provide hardware, audio capture, synchronization, transcription, diarization, and exports. The Executive Support System owns the canonical ingestion contract, provenance, clarification, knowledge links, actions, scheduling, and recovery workflow.

## Alternatives considered

- Build first-party recording hardware and software immediately.
- Make one recorder vendor mandatory.
- Support only manual text capture.

## Consequences

- Manual text, file, email, folder, audio, and transcript ingestion remain universal fallbacks.
- Provider adapters map into one canonical capture object.
- Connector and purchasing priorities are driven by monitored evidence and hands-on testing.