---
layout: default
title: Features
parent: Definition Manager
grand_parent: SIE
nav_order: 1
redirect_from:
  - /sie-definition/features/
---

# Definition Manager Features
{: .no_toc }

Capability catalogue for the Definition Manager, grouped by functional component. Capabilities of the other SIE products live on their own pages — see the [Operator features]({% link sie/operator/features.md %}), the [Definition Blackboard Manager features]({% link sie/definition-blackboard-manager/features.md %}), and the engine-level [SIE Roadmap]({% link sie/roadmap.md %}).

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Milestones

- **Foundation** — implemented in the SIE engine today (real service code).
- **Near-term** — prioritized next (P0, feasibility now).
- **Mid-term** — planned (P1, feasibility next).
- **Future** — projected (P2–P3, later).
- **Exploratory** — research-tier; may evolve substantially or not ship.

Milestones express prioritization and engine reality — not delivery commitments.

---

## Capabilities

The Definition Manager is an implemented engine service — the substrate every domain application builds on.

| Functional component | Representative features | Milestone |
|----------------------|-------------------------|-----------|
| GSM Definitions management RESTful API | Create, read, update, and query every governed GSM definition; live OpenAPI; structured problem responses; isolated tenant schemas | Foundation |
| GSM core & governance grammar | Author the 8 GSM primitives; DNA authoring (Directive / Norm / Ascription); Archetype schema validation | Foundation |
| GSM Definitions lifecycle enforcement | Ascription lifecycle as a validated state machine (DRAFT → … → RETIRED) with referee preconditions | Foundation |
| GSM Definitions retention | Definitions and their history retained as versioned state transitions — nothing governed is silently overwritten or lost | Foundation |
