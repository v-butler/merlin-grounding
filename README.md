# Merlin Grounding

**Authoritative grounding, sanity anchors, and project state for the Merlin assistant system**

This repository exists as the **single source of truth** for the Merlin project.  
Its purpose is to prevent context drift, loss of state, and repeated re-interpretation of decisions over time.

This repo prioritises **stability, clarity, and grounding** over speed or experimentation.

---

## 🧠 Purpose

Merlin is a long-running AI assistant system with:

- a persistent “brain” process
- text and voice interaction via a chat UI
- background services that must remain alive independently of any web server
- an explicit grounding and sanity model

This repository exists to document and anchor:

- what the system is
- how it is expected to behave
- what state the project is currently in
- which decisions are fixed and must not be re-litigated

---

## 📦 How This Repo Works

This repository is **documentation and authority**, not runtime code.

It defines structure, intent, and state.

The intended structure of this repository is:

```
merlin-grounding/
├── README.md              ← Project authority & orientation
├── sanity/                ← Sanity anchors, rules, and logs
├── project/               ← Project state, plans, and decisions
├── runtime/               ← Environment and service grounding
└── CHANGELOG.md           ← High-level project history
```

At any given time, not all folders or files may exist yet.  
Their presence is driven by project phase and necessity.

---

## 🛠 How This Repo Is Used

- This repo is the **authoritative reference** for project state  
- It replaces reliance on memory, chat history, or informal notes  
- It is updated deliberately and incrementally  
- Changes here represent **intentional decisions**, not experiments  

If something is not recorded here, it is **not considered stable or agreed**.

---

## 🛡 Security & Safety Rules

This repository is public by necessity.

It must **never contain**:

- passwords
- API keys
- access tokens
- certificates
- private IP addresses
- environment secrets
- credentials of any kind

Only **structure, logs, decisions, and documentation** belong here.

Runtime secrets are stored **outside** version control.

---

## 📆 Current Project Status

**Phase:** Foundational grounding & stabilisation

**Current focus:**
- Establish authoritative documentation
- Eliminate ambiguity between prototype vs production
- Stabilise background services independently of IIS
- Preserve a working chat + audio pipeline without re-architecting

No new features are being added until stability is confirmed.

---

## 📌 Contribution & Authority

This repository is maintained by the project owner.

- External contributions are not expected
- Pull requests are not required
- Changes are made deliberately and sparingly

This repo exists to **reduce chaos**, not create it.

---

## 🔒 Final Note

This repository is not about speed.  
It is about **continuity, grounding, and control**.

Once something is written here, it becomes part of the project’s reality.

