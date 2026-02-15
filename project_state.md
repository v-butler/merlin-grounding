# Project State — Merlin

This document defines the **current, authoritative state** of the Merlin project.

It answers:
- where the project is right now
- what is actively being worked on
- what is explicitly not being worked on
- what must be true before moving forward

If something is not listed here, it is **not active work**.

---

## Current Phase

**Phase:** Foundational grounding & stabilisation

The project is transitioning from prototype behaviour to production-grade stability.
No new features are being added during this phase.

---

## Primary Objective (Singular)

**Establish a stable, persistent Merlin runtime that does not die unexpectedly.**

All current work must directly support this objective.

---

## Active Focus

- Externalise project state and memory into GitHub
- Eliminate ambiguity between prototype vs production behaviour
- Define and enforce sanity rules
- Prevent background processes from being killed by web server lifecycles

---

## What Is Currently Working

- Chat UI text input → brain → text output
- Brain responses are correctly generated
- Text-to-speech output is functioning
- GitHub grounding repository is established
- Sanity anchor, rules, and log are in place

---

## What Is Currently Broken or Unstable

- Microphone / speech-to-text input is not yet stable
- Background Python processes are being terminated unexpectedly
- IIS recycling interferes with long-running components
- Runtime lifecycle management is not yet hardened

---

## Explicit Non-Goals (For This Phase)

The following are **not** being worked on right now:

- Rebuilding or replacing the brain
- Introducing new AI models
- UI redesigns or visual polish
- Feature expansion
- Performance optimisation
- Cross-device enhancements

Any work in these areas is deferred.

---

## Immediate Next Steps

The next steps, in order:

1. Define how Merlin’s background components are run persistently on Windows
2. Decouple core logic from IIS lifecycle completely
3. Restore microphone input **after** runtime stability is achieved
4. Confirm end-to-end text + voice loop under stable conditions

Steps must be completed sequentially.

---

## Blockers

- No formal Windows service or task configuration exists yet for Merlin
- PowerShell / environment state needs verification (deferred until runtime work begins)

---

## Stop Conditions

Work must pause if:

- the primary objective becomes unclear
- multiple competing fixes are attempted
- changes are made without updating grounding documents
- fatigue or frustration materially affects judgement

---

## Status Summary

Merlin is **not broken**, but **not yet hardened**.

The system works functionally but lacks lifecycle stability.
Current work is focused on making it reliable before expanding capabilities.

