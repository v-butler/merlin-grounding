# Project Plan — Merlin

This document defines the **high-level execution plan** for the Merlin project.

It is dependency-driven, not time-driven.
Phases are completed sequentially.

Work does not advance to a later phase until the current phase exit criteria are met.

---

## Phase 1 — Grounding & Authority (COMPLETED)

### Purpose
Establish a single source of truth and eliminate contextual drift.

### Scope
- GitHub grounding repository
- README as project authority
- Sanity anchor, rules, and log
- Project state definition

### Exit Criteria
- Grounding documents exist and are committed
- Sanity system is operational
- Project state is explicit

**Status:** Complete

---

## Phase 2 — Runtime Stabilisation (CURRENT)

### Purpose
Ensure Merlin’s core processes remain alive and stable under normal operating conditions.

### Scope
- Identify all long-running Merlin components
- Remove dependency on IIS lifecycle
- Run core logic as:
  - Windows service, or
  - Scheduled task with persistence guarantees
- Verify behaviour across:
  - browser close
  - user logoff
  - idle periods
  - IIS recycling

### Explicit Exclusions
- No feature additions
- No model changes
- No UI redesigns

### Exit Criteria
- Brain process survives without manual intervention
- Background services do not terminate unexpectedly
- System behaviour is predictable and repeatable

**Status:** In progress

---

## Phase 3 — Audio Input Recovery

### Purpose
Restore microphone input on top of a stable runtime foundation.

### Scope
- Speech-to-text pipeline
- Microphone device handling
- Input → brain → response loop

### Dependencies
- Phase 2 complete

### Exit Criteria
- Voice input works consistently
- No regression to runtime stability

---

## Phase 4 — Hardening & Reliability

### Purpose
Reduce fragility and improve resilience.

### Scope
- Error handling
- Graceful restarts
- Logging improvements
- Recovery from partial failures

### Dependencies
- Phases 2 and 3 complete

---

## Phase 5 — Feature Expansion (DEFERRED)

### Purpose
Introduce new capabilities once the system is stable.

### Examples
- UI improvements
- Additional modules
- Multi-device enhancements
- Performance optimisation

### Dependencies
- All previous phases complete
- Explicit decision to proceed

---

## Plan Enforcement Rules

- Phases are not skipped
- Exit criteria must be met before progression
- Deviations require documentation
- “Just testing something” belongs outside production paths

---

## Purpose Reminder

This plan exists to:
- prevent sideways movement
- keep effort aligned
- protect already completed work

Progress is defined by **completion**, not activity.

