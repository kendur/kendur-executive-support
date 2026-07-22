# Capture and Ingestion

## Principle

**Capture must be fast, source-agnostic, and tolerant of incomplete thought.**

The system accepts fragments first and separates capture from later clarification.

## Universal inbox

All capture routes feed one logical Inbox. A user may have several devices or services, but should not have to review several independent capture queues.

An Inbox item is source material. It may later become an action, project, decision, waiting-for item, reference, or intentional discard.

## Supported source classes

A source does not need to produce text before ingestion. The system may accept:

- manual text or a short fragment;
- a spoken thought stream;
- raw audio;
- a vendor transcript or summary;
- meeting notes;
- email;
- a link or web clip;
- an image or screenshot;
- a PDF, document, spreadsheet, or other file;
- a calendar event;
- an automation payload;
- a future source that can map into the canonical capture contract.

Specialized products such as PLAUD, Fieldy, Pocket, Omi, Bee, and future devices are optional adapters. A phone, browser, or manual form remains sufficient.

## Thought-stream capture

Rapid associative thought is a first-class capture pattern. A user may speak in fragments, change direction, interrupt themselves, or lose a thought mid-sentence.

The source stream should be preserved. Optional processing may:

- identify likely idea boundaries;
- preserve unfinished threads;
- extract possible commitments or decisions;
- avoid converting every sentence into a task;
- present fragments later for clarification.

## Required capture fields

| Field | Description | Required |
|---|---|---|
| `capture_id` | Stable internal identifier | Yes |
| `title` | Short label; may be generated from a fragment | Yes |
| `raw_content` | Original text, transcript, or note | No |
| `source_type` | Manual, voice, audio, email, meeting, web, file, automation, or other | Yes |
| `source_provider` | Vendor or application when known | No |
| `source_reference` | Link or external record ID | No |
| `captured_at` | Source timestamp | Yes |
| `profile` | Personal, Work, or Unknown | Recommended |
| `status` | Captured on creation | Yes |
| `attachments` | Files, audio, images, or links | No |

Incomplete provenance remains acceptable. Clarification may add it later.

## Profile handling

The public field is **Profile**, with default values:

- Personal
- Work
- Unknown

Employer names belong in private configuration, not in public template fields or examples.

## Conversation records

Recorded conversations should preserve:

- source device or service;
- start and end time;
- transcript and timestamped segments when available;
- speaker labels;
- vendor summary and action suggestions;
- original audio reference;
- related meeting or project;
- Personal or Work profile;
- processing and review status.

Derived records should link back to the source conversation rather than replacing it.

Possible extracted classifications include:

- explicit commitment;
- assigned action;
- possible action;
- decision;
- waiting for;
- reference;
- unfinished thread;
- unclear.

## Canonical adapter contract

Adapters normalize a source into a provider-neutral capture object. A simplified example:

```json
{
  "schema_version": "1.0",
  "capture_id": "uuid",
  "source_type": "conversation",
  "source_provider": "provider-name",
  "source_reference": "external-id-or-url",
  "captured_at": "2026-07-22T08:00:00-04:00",
  "profile": "Work",
  "title": "Short capture title",
  "raw_content": "Original text or transcript",
  "attachments": []
}
```

The adapter may be implemented in n8n, Zapier, Make, Tasker, a vendor API, email, a monitored folder, or a future first-party service. The contract remains stable when the implementation changes.

## Clarification

Capture does not require a project, priority, due date, task breakdown, or complete wording. Clarification later determines:

- what the item means;
- whether action exists;
- the desired outcome;
- the next visible action;
- the appropriate profile and project;
- any due date or scheduled work;
- what evidence or context should remain attached.

The interface must make this workflow understandable without external instructions.