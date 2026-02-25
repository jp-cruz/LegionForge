# Legionforge

**A local-first, security-native AI agent framework.**

> 🚧 Under active development. Public release coming when Phase 1 is complete.

---

## What Is This?

Legionforge is an open-source AI agent framework built on [LangGraph](https://github.com/langchain-ai/langgraph), designed to run on local hardware with optional cloud LLM fallback. Security is built into the foundation — not bolted on later.

**The one-line pitch:** The hardened, self-hosted alternative for teams who need real security guarantees from their AI agents — and a security layer that other agent frameworks can plug into.

---

## The Problem

Most AI agent frameworks treat security as an afterthought. Tool calls are unvalidated. Credentials leak into logs. Prompt injection goes undetected. Multi-agent systems cascade failures across the entire pipeline. Resource bombs drain API budgets in minutes.

Legionforge is designed from the ground up to address these threats — with deterministic security checks, cryptographic tool signing, task-scoped privilege tokens, and a human approval gate on every security mutation.

---

## Key Design Principles

**Security in the hot path is deterministic.** No LLM calls during security checks. Fast, auditable, and immune to prompt injection by design.

**Fail-safe is tiered, not binary.** High-confidence threat → halt and quarantine. Ambiguous → sandbox and retry. Soft failure → degrade and continue.

**Privilege follows the task, not the agent.** Short-lived task tokens scoped to exactly what the current run requires. Sub-agents get narrower derived tokens. Blast radius is always bounded.

**Human gates on all mutations.** No component autonomously changes security rules, promotes tools, or escalates privileges. Ever.

---

## Threat Classes Addressed

| Threat | Severity |
|---|---|
| Tool Poisoning — malicious instructions in tool metadata | 🔴 Critical |
| Rug-Pull — tool changes behavior after trust is established | 🔴 Critical |
| Prompt Injection (direct + indirect) | 🔴 Critical |
| Resource Bomb / Economic DOS | 🟠 High |
| Credential Theft | 🟠 High |
| RAG / Memory Poisoning | 🟠 High |
| Multi-Agent Cascade | 🟠 High |
| Supply Chain | 🟡 Medium |

---

## Roadmap

| Phase | What Gets Built | Status |
|---|---|---|
| 0 — Infrastructure | PostgreSQL, pgvector, LLM factory, health server, smoke tests | ✅ Complete |
| 1 — First Agent + Security Foundations | Researcher agent, tool hash validation, cost estimation, threat logging | 🔄 Active |
| 2 — Containerization + Guardian | Docker stack, Guardian security sidecar, immutable audit log | ⬜ Planned |
| 3 — ACLs + Sub-Agents | Task tokens, role definitions, orchestrator pattern | ⬜ Planned |
| 4 — Adaptive Threat Intelligence | Threat Analyst agent, adaptive Guardian rules, AI-BOM | ⬜ Planned |
| 5 — Tool Library + Signing | Crystallized tools, cryptographic signing, containerized tool images | ⬜ Planned |
| 6 — PentestAgent | Air-gapped red-team bot, continuous security regression | ⬜ Planned |

---

## Hardware Target

Designed to run on Apple Silicon (M4 Mac Mini, 16GB RAM). Full Phase 6 deployment peaks at ~8–9GB RAM. No cloud infrastructure required.

---

## Status

Code is being developed privately and will be published here when Phase 1 is complete. Watch this repo for updates.

**Website:** [legionforge.org](https://legionforge.org)

---

## Author

**Jp Cruz**
[github.com/jp-cruz](https://github.com/jp-cruz)

---

## License

[AGPL-3.0](./LICENSE) — free to use, modify, and distribute. Modifications must be open-sourced under the same license.
