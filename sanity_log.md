# Sanity Log — Merlin Project

This file is an **append-only operational log**.

It records the actual state of the Merlin project at specific points in time.
Its purpose is to replace memory, reduce confusion, and preserve continuity.

Entries should be factual, concise, and chronological.

---

## Log Entry Format

Each entry must follow this structure:

- **Date:**
- **Time:**
- **Scan type:** (morning / afternoon / ad-hoc)
- **Current focus:**
- **What is working:**
- **What is broken or unstable:**
- **Recent changes:**
- **Blockers:**
- **Decision:** (continue / pause / stop)
- **Notes:**

---

## Entries

### Entry 002

- **Date:** 2026-02-15
- **Time:** 14:48
- **Scan type:** ad-hoc
- **Current focus:** Runtime stabilisation and cross-device access
- **What is working:**
  - Merlin brain and TTS services running persistently via Windows Scheduled Tasks
  - Chat UI works on Bob (Chrome)
  - Chat UI works on iPad (Chrome)
  - Chat UI works on iPhone (Safari and Chrome)
  - Safari issues on iPad resolved
- **What was broken or unstable:**
  - iPad Safari failed to connect despite working backend
- **Root cause identified:**
  - Safari iPad aggressive JS caching / poisoned execution state
- **Resolution:**
  - Forced Safari cache purge and JS cache-busting on `chat.js`
- **Recent changes:**
  - Replaced hard-coded loopback addresses in frontend
  - Added cache-busting query to chat.js script include
- **Decision:** continue
- **Notes:**
  - Significant stability milestone achieved
  - System now behaves consistently across devices...
 
  - “Located legacy Merlin identity definition in config/identity_prompt.txt.
Not currently loaded by merlin_engine.py.
Identity injection likely removed during runtime refactor.”



### Entry 001

- **Date:** 2026-02-15
- **Time:** 15:10
- **Scan type:** ad-hoc
- **Current focus:** Establish GitHub grounding and sanity structure
- **What is working:**
  - GitHub repository created
  - README established as project authority
  - Sanity anchor and sanity rules defined
- **What is broken or unstable:**
  - Background runtime stability not yet addressed
  - Audio input pipeline not yet finalised
- **Recent changes:**
  - Introduced public GitHub repo as external project memory
  - Created sanity anchor and rules
- **Blockers:**
  - None at this stage
- **Decision:** continue
- **Notes:**
  - Grounding phase in progress
  - Cognitive load reduced by externalising state




---


## Logging Rules

- New entries are added to the **top** of the Entries section
- Existing entries are never edited or removed
- Corrections are made by adding a new entry
- Logs reflect reality, not intention

---

## Purpose Reminder

This log exists to:
- prevent loss of context
- stop circular work
- provide a factual timeline
- support deliberate progress

If the log is not updated, work is considered provisional.

