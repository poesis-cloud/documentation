---
layout: default
title: Features
parent: Definition Blackboard Code Sourcer
grand_parent: ITIP
nav_order: 1
redirect_from:
  - /itip-blackboard-sourcer/features/
---

# ITIP Blackboard Sourcer Features
{: .no_toc }

Capability catalogue for the ITIP Blackboard Sourcer.

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
