# Capture and Ingestion

This document describes how information enters the Executive Support System—the capture layer.

---

## Principle

**Capture must be fast and tolerate incomplete thoughts.**

A half-formed idea captured is more valuable than a perfect idea forgotten. The system must never punish a user for capturing something imperfect, ambiguous, or unresolved.

---

## The Inbox

All captured items land in a single **Inbox** in Notion. The Inbox is the system's entry point regardless of capture source.

Items in the Inbox are unprocessed. They carry a source tag, a timestamp, and whatever content was provided. They are not yet actions, projects, or reference material. Triage is a separate, deliberate activity that happens later.

---

## Capture Sources

The system is capture-source-agnostic. Any source that can produce text can feed the Inbox. No specific source is required.

### Manual Entry

The simplest source. The user creates a new Inbox item directly in Notion.

**When to use:** When near a computer or phone with the Notion app, and the item can be typed quickly.

### Voice Recording and Transcription

A voice recorder (phone voice memo, PLAUD, Omi, Fieldy, or any device) captures audio. The audio is transcribed (manually or automatically) and the transcript is added to the Inbox.

**When to use:** When typing is impractical—walking, driving, or when speaking is faster than writing.

The transcript is stored as the item content. The source tag indicates it came from voice. The provenance field records which device or session, if known.

### Email

An email is forwarded or automatically routed to the Inbox. The email subject becomes the item title; the body (or a summary) becomes the content.

**When to use:** When an email represents an obligation, decision, or item that needs tracking outside of email.

### Meeting Notes and Transcripts

Notes or a transcript from a meeting are added to the Inbox as a single item or as a batch of items. The meeting name and date serve as provenance.

**When to use:** After any meeting where commitments were made, questions arose, or decisions were deferred.

### Read-Later and Saved Articles

Links and articles saved in a read-later service (Pocket or equivalent) can be routed to the Inbox for triage into Reference or Action.

**When to use:** When a saved article contains something that needs to be acted on, not just read.

### Files and Documents

Uploaded files, PDFs, or attached documents can be linked to an Inbox item for later processing.

**When to use:** When a document contains obligations or decisions that need tracking.

### Automation-Routed Items

Items routed automatically by an automation adapter (n8n, Zapier, Make, Tasker, or other). The adapter creates an Inbox item via the Notion API.

**When to use:** Whenever a source can be reliably automated and the volume justifies it.

---

## Required Fields for Every Inbox Item

| Field | Description | Required |
|---|---|---|
| Title | A short label for the item—can be a fragment | Yes |
| Content | The raw captured text, transcript, or note | No |
| Source | How it arrived (voice, email, meeting, manual, automation) | Yes |
| Provenance | Where it came from (meeting name, person, project) | Recommended |
| Captured at | Timestamp | Yes (auto) |
| Status | Always "Inbox" on creation | Yes (auto) |
| Context | Personal or Work | Recommended |

Items that arrive without full provenance are still valid. The restart cue and provenance can be added during triage.

---

## Capture Quality Levels

Captured items arrive at different levels of completeness. All are acceptable:

| Level | Description | Example |
|---|---|---|
| Fragment | A few words or a title only | "Follow up with Alex" |
| Note | A sentence or short paragraph | "Alex mentioned budget approval is blocked on Finance sign-off" |
| Raw | An unedited transcript or forwarded email | A 10-minute voice memo transcript |
| Structured | A well-described item with context | "Meeting with Alex re Q3 budget — decision needed on Finance approval path before Friday" |

The system handles all four. The triage step converts fragments and raw content into structured items.

---

## What Happens Next

Items sit in the Inbox until triaged. Triage is described in the workflow documentation (to be written in Phase 1).

The Inbox should be reviewed regularly—at minimum once per day during active use. Items in the Inbox do not represent actions yet.

---

## Automation Adapter Interface

When an adapter (n8n, Zapier, Make, or other) creates an Inbox item, it should provide:

- **title** — string, required
- **content** — string, optional
- **source** — one of: `voice`, `email`, `meeting`, `web`, `file`, `automation`, `manual`
- **provenance** — string, optional
- **context** — one of: `Personal`, `Work`, `Unknown`
- **captured_at** — ISO 8601 timestamp, optional (defaults to now)

The adapter is responsible for transforming its source format into this schema. The Notion API call is the boundary between the adapter and the system.
