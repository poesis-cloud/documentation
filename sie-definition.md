---
layout: default
title: SIE Definition
nav_order: 2
---

# SIE Definition
{: .no_toc }

> **In construction.** This product's documentation is being written. The capability catalogue below reflects the design-time backlog and the current engine reality.

**SIE Definition** is the core of the Systemic Intelligence Engine: the Definition Manager that hosts GSM, the Operator rule runtime, and their database. It is the most mature part of the platform — the capabilities marked **Foundation** are backed by real, running service code today. It implements the open **[GSM standard]({% link gsm-manifesto.md %})**.

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

## Foundational services

The Definition Manager and the Operator are implemented engine services — the substrate every domain application builds on.

| Functional component | Representative features | Milestone | Usage scenario |
|----------------------|-------------------------|-----------|----------------|
| Definition Manager — GSM core | Author the 8 GSM primitives; DNA authoring (Directive / Norm / Ascription); Ascription lifecycle (DRAFT → … → RETIRED); Archetype schema validation | Foundation | — |
| Operator — rule runtime | Norm / Mechanism rule evaluation (Starlark sandbox); Effector / Receptor dispatch; closed-loop control | Foundation | — |

## Governance intelligence (analytics)

The analytical layer SIE will expose over the governed model. None are implemented yet.

| Functional component | Representative features | Milestone | Usage scenario |
|----------------------|-------------------------|-----------|----------------|
| Descriptive analytics | State monitoring & audit trail; structural observation (coupling, critical path); temporal observation (trend / drift detection) | Near-term | — |
| Diagnostic analytics | Causal attribution & root-cause; anomaly detection; constraint conflict / coherence / gap diagnostics | Mid-term | — |
| Predictive analytics | Forecasting; blast-radius & risk propagation; what-if / Norm simulation | Mid-term | — |
| Prescriptive analytics | Remediation recommendation; homeostasis (closed-loop); LLM-assisted DNA bootstrap | Near-term | — |
| Assurance & safety | Provenance & lineage; uncertainty / confidence; LLM-output assurance; automation guardrails | Near-term | — |
| Emergence & cross-domain inference | Emergence detection; code → business cross-domain impact | Exploratory | — |

## Environmental context and system presets

| Functional component | Representative features | Milestone | Usage scenario |
|----------------------|-------------------------|-----------|----------------|
| System presets | Regulatory / geopolitical / industry-standard presets; preset import & instantiation; preset composition & conflict detection | Near-term | — |
