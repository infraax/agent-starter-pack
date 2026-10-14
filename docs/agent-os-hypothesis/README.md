# Independent Agent OS Architecture Hypothesis

> Status: research/design proposal only. No runtime implementation is supplied here.
>
> **Source caveat:** This first index and its accompanying proposal were authored from the architecture context available in this conversation, the `infraax/Polder` design documents, and the PARKING research source in `infraax/NAP-corpus`. The attached `merged.md` itself was not discoverable in this session, so this is not yet a complete line-by-line translation of that file. Replace the source ledger with exact research references once `merged.md` is available.

## Intent
Design from zero an agent-first OS layer for heterogeneous Linux machines and clusters. Agents are the system's primary users; the human is a principal setting goals, risk boundaries and reserved approvals. The initial workload domain is software development, with later support for research/data and infrastructure operations.

## Architecture thesis
Build a **federated control plane with a deterministic, append-only authority ledger and node-local execution**, rather than a single giant agent or a fully distributed consensus of LLM decisions. Use event-driven scheduling, typed contracts, isolated workspaces, capability-scoped access, independent verification and risk-gated adoption. During network partitions, nodes may continue only explicitly safe local work; authority-sensitive mutations require a valid epoch/lease and cannot be decided independently by partitioned control planes.

## Documents
- [01 — Vision, scope and requirements](01-vision-requirements.md)
- [02 — Reference architecture](02-reference-architecture.md)
- [03 — Roles and organisation](03-roles-and-organisation.md)
- [04 — Runtime and communication](04-runtime-communication.md)
- [05 — Data model and contracts](05-data-model-contracts.md)
- [06 — Resource governance](06-resource-governance.md)
- [07 — Authority, failures and security](07-authority-reliability-security.md)
- [08 — Controlled self-improvement](08-controlled-self-improvement.md)
- [09 — Technology choices](09-technology-choices.md)
- [10 — Architecture decision records](10-adrs.md)
- [11 — Risk register and validation plan](11-risks-validation.md)
- [12 — Source traceability and relation to Polder](12-traceability-polder.md)
- [Diagrams index](diagrams/README.md)

## Important distinction
Polder, Aparatus, RWS 2.0 and PARKING are comparative sources and precedent—not assumed implementation dependencies. This proposal is intentionally independent and may keep, change or reject their choices.

## Reading order
Read 01 → 02 → 03 → 04–08 → 09–12. The diagrams are part of the design contract, not decorative summaries.