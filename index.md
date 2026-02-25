---
title: Legionforge
---

# Legionforge
### Local-First. Security-Native. AI Agents You Can Trust.

**A hardened AI agent framework designed for teams that require real security guarantees.**

🚧 Phase 1 in active development. Public release coming soon.

[View Project on GitHub](https://github.com/jp-cruz/LegionForge)

---

## Why Legionforge Exists

Modern AI agent frameworks ship fast and secure later — if ever.  
Legionforge flips that model.

Security is enforced in the execution path, not layered on afterward.  
Every tool invocation, privilege boundary, and mutation is governed by deterministic controls.

**Result:** predictable, auditable, failure-contained AI systems.

---

## Core Capabilities

### Deterministic Security Enforcement
No LLM involvement in security decisions.  
Controls are fast, auditable, and resistant to prompt injection by design.

### Task-Scoped Privilege Model
Permissions follow the task — not the agent.  
Short-lived tokens define exact capability boundaries for each execution.

### Cryptographic Tool Trust
Tools are validated by hash and signature.  
Behavior changes cannot occur silently.

### Human-Governed Mutations
Security policy changes require explicit approval.  
Autonomous privilege escalation is impossible by design.

---

## Threat Classes Addressed

| Threat | Severity |
|---|---|
| Tool Poisoning | Critical |
| Rug-Pull Tool Behavior | Critical |
| Prompt Injection (Direct + Indirect) | Critical |
| Resource Exhaustion / Economic DOS | High |
| Credential Exposure | High |
| RAG / Memory Poisoning | High |
| Multi-Agent Cascade Failure | High |
| Supply Chain Risk | Medium |

---

## Architecture Philosophy

Security must operate in the **hot path** of execution.  
Failure handling must be **tiered, not binary**.  
Privilege must be **bounded and ephemeral**.  
Mutation must always be **human-governed**.

---

## Roadmap

| Phase | Focus | Status |
|---|---|---|
| 0 — Infrastructure | Core services, storage, model factory | Complete |
| 1 — First Agent + Security Foundation | Researcher agent, validation, logging | Active |
| 2 — Guardian Security Layer | Containerized execution, audit log | Planned |
| 3 — Access Control Model | Task tokens, orchestrator pattern | Planned |
| 4 — Adaptive Threat Intelligence | Threat Analyst agent | Planned |
| 5 — Signed Tool Ecosystem | Verified tool distribution | Planned |
| 6 — Continuous Security Testing | Air-gapped red-team agent | Planned |

---

## Deployment Target

Designed for local execution on Apple Silicon.  
No mandatory cloud dependency.  
Security guarantees do not depend on external infrastructure.

---

## Project Status

Codebase currently private during Phase 1 hardening.  
Public repository release planned upon completion.

Follow development progress on GitHub.

---

## Author

**Jp Cruz**  
Security-focused AI systems engineering

---

## License

AGPL-3.0 — open source with reciprocal guarantees.
