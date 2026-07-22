# AI Usage Policy

AI is used both in project development and as an optional product capability.

## Development transparency

AI-assisted tools may support research, planning, documentation, code, testing, and review. AI output is treated as a draft. Human maintainers remain accountable for accepted architecture, factual claims, security, licensing, and releases.

Contributors should disclose material AI assistance in pull requests.

## Product principle

The complete core system works without AI. Users may choose:

- no AI;
- a hosted provider;
- a local model;
- different providers for different capabilities;
- a future managed service.

Provider-specific configuration belongs in adapters.

## Optional capabilities

AI may assist with:

- summarization;
- action and decision extraction;
- profile or project suggestions;
- next-action suggestions;
- blocker identification;
- restart cues;
- review assistance;
- related-context retrieval;
- setup and configuration guidance.

Each capability should have a manual path where practical.

## AI Guide Pack

The planned AI Guide Pack is not one enormous prompt. It is a portable set of versioned artifacts:

- a core role and behavior prompt;
- a concise template reference;
- progressive onboarding questions;
- skill-level and preference settings;
- supported capability prompts;
- test cases and expected behaviors;
- a canonical update link.

It should work with Notion AI, ChatGPT, Claude, compatible local models, and future providers where their capabilities allow.

Onboarding must remain progressive. The guide asks only what is needed for the next decision and learns additional preferences through use.

## Graduated autonomy

Default behavior is advisory. When explicitly configured, AI and deterministic automation may perform routine, reversible actions such as applying known fields, creating draft records, or routing a capture by a trusted rule.

Human approval is required for consequential, destructive, conflicting, or external actions, including:

- deleting source records;
- sending communication;
- resolving ambiguous profile or project conflicts;
- changing accepted project direction;
- changing licensing;
- committing money or making external commitments.

Every derived record should preserve provenance and review state.

## Development disclosure log

| Date | Tool and use |
|---|---|
| 2026-07-22 | GitHub Copilot Coding Agent drafted the initial documentation foundation in PR #1; the maintainer reviewed and accepted it. |
| 2026-07-22 | ChatGPT supported research, architecture, issue definition, and the follow-up alignment PR. |