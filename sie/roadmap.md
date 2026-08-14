---
layout: default
title: Roadmap
parent: SIE
nav_order: 4
---

# SIE Roadmap
{: .no_toc }

Engine-level capabilities planned across the SIE products — the analytical and contextual layers SIE will expose over the governed model. Product-scoped capabilities live on each product's Features page: [Definition Manager]({% link sie/definition-manager/features.md %}), [Operator]({% link sie/operator/features.md %}), [Definition Blackboard Manager]({% link sie/definition-blackboard-manager/features.md %}).

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

## Governance intelligence (analytics)

The analytical layer SIE will expose over the governed model. None are implemented yet.

| Functional component | Representative features | Milestone |
|----------------------|-------------------------|-----------|
| Descriptive analytics | State monitoring & audit trail; structural observation (coupling, critical path); temporal observation (trend / drift detection) | Near-term |
| Diagnostic analytics | Causal attribution & root-cause; anomaly detection; constraint conflict / coherence / gap diagnostics | Mid-term |
| Predictive analytics | Forecasting; blast-radius & risk propagation; what-if / Norm simulation | Mid-term |
| Prescriptive analytics | Remediation recommendation; homeostasis (closed-loop); LLM-assisted DNA bootstrap | Near-term |
| Assurance & safety | Provenance & lineage; uncertainty / confidence; LLM-output assurance; automation guardrails | Near-term |
| Emergence & cross-domain inference | Emergence detection; code → business cross-domain impact | Exploratory |

## Environmental context and system presets

| Functional component | Representative features | Milestone |
|----------------------|-------------------------|-----------|
| System presets | Regulatory / geopolitical / industry-standard presets; preset import & instantiation; preset composition & conflict detection | Near-term |
