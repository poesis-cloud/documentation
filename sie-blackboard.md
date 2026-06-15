---
layout: default
title: SIE Blackboard
nav_order: 3
---

# SIE Blackboard
{: .no_toc }

> **In construction.** This product's documentation is being written. The capability catalogue below reflects the design-time backlog and the current engine reality.

**SIE Blackboard** is the collaborative definition-sourcing service — the server side of GSM definition sourcing. It accepts validated contributions, enforces the blackboard seal lifecycle, and keeps an append-only audit ledger. It is built on the open **[GSM standard]({% link gsm/index.md %})** and receives contributions from clients such as the **[ITIP Blackboard Sourcer]({% link itip-blackboard-sourcer.md %})**.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Milestones

- **Foundation** — implemented today (real service code).
- **Near-term** — prioritized next (P0, feasibility now).
- **Mid-term** — planned (P1, feasibility next).
- **Future** — projected (P2–P3, later).

Milestones express prioritization and engine reality — not delivery commitments.

---

## Capabilities

| Functional component | Representative features | Milestone | Usage scenario |
|----------------------|-------------------------|-----------|----------------|
| Blackboard lifecycle | Blackboard seal state machine (OPEN → SEALED → BYTE_STABLE); isolation invariant (sealed boards immutable) | Foundation | — |
| Contribution validation | Contribution posting & schema validation against the referenced Panel; rejection of invalid contributions before persistence | Foundation | — |
| Audit ledger | Append-only audit entries, transactional with each mutation; immutable record of every blackboard change | Foundation | — |
| Panel & contribution model | Panel declaration; confidence / provenance envelopes; sealed byte-stable contribution streams | Foundation | — |
