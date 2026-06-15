---
layout: default
title: ITIP Blackboard Sourcer
nav_order: 5
---

# ITIP Blackboard Sourcer
{: .no_toc }

> **In construction.** This product's documentation is being written. The capability catalogue below reflects the design-time backlog and the current engine reality.

The **ITIP Blackboard Sourcer** ingests external IT artifacts — code, API contracts, infrastructure, and (later) legal and standards texts — and turns them into governed GSM definitions, posting them as contributions to the **[SIE Blackboard]({% link sie-blackboard.md %})**. Every sourced definition enters the model as a DRAFT, carrying its provenance, so a human remains the trust boundary. It is built on the open **[GSM standard]({% link gsm/index.md %})**.

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
| Collaborative contribution path | Blackboard contribution posting; confidence / provenance envelopes; sealed byte-stable streams | Foundation | — |
| Core sourcing pipeline | Inventory & classification; deterministic + LLM extraction (hybrid); merge / deduplicate; GSM-JSON output with provenance (all output starts DRAFT) | Near-term | — |
| IT-domain source adapters | Git repository (Java / Spring → Mechanism rules); API contracts (OpenAPI / gRPC / AsyncAPI); infrastructure (Helm / Dockerfile / Terraform) | Mid-term | — |
| Legal & regulatory adapters | EUR-Lex legislation (article → Directive, obligation → Norm); regulation-as-system modeling; multi-language | Future | — |
| Standards adapters | ISO/IEC, NIST CSF, CIS (SHALL / SHOULD → Directive, control → Norm); standard-as-system modeling | Future | — |
