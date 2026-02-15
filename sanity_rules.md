# Sanity Rules — Merlin Project

This document defines **how sanity is maintained** across the Merlin project.

Its purpose is to:
- detect drift early
- preserve continuity
- reduce cognitive overload
- prevent circular or regressive work

These rules are operational, not philosophical.

---

## 1. Sanity Scan Definition

A **sanity scan** is a deliberate snapshot of project reality.

Each scan records:
- current focus
- what is working
- what is broken
- what changed since the last scan
- why work is continuing or stopping

Sanity scans exist to replace memory with record.

---

## 2. Sanity Scan Schedule

Sanity scans are performed at **minimum**:

- **Late morning scan** (≈ 10:00–11:00)
- **Early afternoon scan** (≈ 13:00–14:00)

Additional scans may occur:
- after major fixes
- before stopping work
- when confusion or frustration rises

If a scan is skipped, the reason should be noted in the next log entry.

---

## 3. Where Sanity Scans Are Recorded

All sanity scans are recorded in:

```
sanity/sanity_log.md
```

Entries are:
- append-only
- chronological
- factual
- non-judgemental

This file is the historical record of project state.

---

## 4. Drift Detection Rules

Drift is considered present if **any** of the following occur:

- goals change mid-session without documentation
- previously working components are reworked without cause
- architecture is questioned without new evidence
- multiple parallel fixes are attempted simultaneously
- frustration increases without a clear technical blocker

When drift is detected, work must pause.

---

## 5. Mandatory Pause Conditions

Work **must stop** if:

- the current goal cannot be clearly stated
- more than one primary task is active
- changes are being made “just to try something”
- the system state is no longer understood
- fatigue or irritation is materially affecting judgement

Stopping is considered a **protective action**, not failure.

---

## 6. Resume Conditions

Work may resume only when:

- a new sanity scan is recorded
- the active task is singular and explicit
- the next action is clearly defined
- the expected outcome is understood

If these conditions are not met, further work is deferred.

---

## 7. Rule Enforcement

These rules apply equally regardless of:
- urgency
- enthusiasm
- perceived simplicity of a change

Breaking sanity rules creates more work later.

---

## 8. Purpose Reminder

These rules exist to:
- protect progress
- preserve mental bandwidth
- keep Merlin evolving deliberately

They are not optional.
They are part of the system.

