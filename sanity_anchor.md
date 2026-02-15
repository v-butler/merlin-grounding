# Sanity Anchor — Merlin Project

This document defines the **non-negotiable grounding truths** for the Merlin project.

Its purpose is to prevent:
- context drift
- circular re-discussion
- accidental re-architecture
- loss of continuity between sessions

Anything written here is considered **authoritative**.

If a statement in this file becomes invalid, it must be **explicitly amended here** before any other work proceeds.

---

## 1. Core Project Identity

- **Project name:** Merlin
- **Nature:** A persistent AI assistant system (not a demo, not a toy)
- **Intent:** Long-running, stable, user-owned assistant with text and voice interaction
- **Status:** Transitioning from prototype to production-grade stability

Merlin is not rebuilt casually.  
Merlin evolves deliberately.

---

## 2. Canonical Architecture Principles

The following principles are fixed unless explicitly revised here:

1. Merlin has a **persistent brain process**
2. The brain **must not depend on a web server lifecycle**
3. UI components (web, tablet, browser) are **clients**, not hosts
4. Background logic must survive:
   - browser closure
   - IIS recycling
   - user logoff
   - idle periods

Any architecture that violates these principles is considered **invalid**.

---

## 3. Web Server Role (IIS)

- IIS is treated as **dumb glass**
- IIS serves:
  - static files
  - UI
  - JavaScript
- IIS does **not** own:
  - brain logic
  - audio pipelines
  - long-running Python processes

IIS recycling is expected behaviour and must not affect Merlin’s core functionality.

---

## 4. Runtime Reality

- The operating environment is **Windows**
- Background components are expected to run as:
  - Windows services, or
  - scheduled tasks configured to persist independently of login state

Prototype-style “run from terminal and hope” execution is no longer acceptable for core components.

---

## 5. What Is Considered “Working”

The following definitions apply:

- **Chat working:**  
  Text input → brain → text output visible in UI

- **Voice output working:**  
  Brain response → TTS → audible playback

- **Voice input working:**  
  Microphone → STT → text → same brain endpoint

Voice input is the **last stage**, not the first.

---

## 6. What Is Explicitly NOT Happening

Unless this file changes, the following are off the table:

- Rebuilding the brain from scratch
- Introducing new models “just to test”
- Re-architecting without a demonstrated failure
- Mixing prototype experiments into production paths
- Moving goalposts mid-session

Stability takes priority over novelty.

---

## 7. Source of Truth Hierarchy

When conflicts occur, authority is resolved in this order:

1. This file (`sanity_anchor.md`)
2. Other documents in `merlin-grounding`
3. Git commit history
4. Live system behaviour
5. Conversation memory

If it isn’t written down, it isn’t binding.

---

## 8. Change Control Rule

Any of the following **must** result in an update to this file:

- Architectural changes
- Environment changes
- Lifecycle changes
- Redefinition of “production”
- Introduction of new always-on components

If the change is important enough to implement, it is important enough to document here.

---

## 9. Purpose Reminder

This file exists to:
- protect project continuity
- reduce cognitive load
- prevent re-litigation of settled ground
- keep Merlin moving forward without chaos

It is not a suggestion.
It is an anchor.

