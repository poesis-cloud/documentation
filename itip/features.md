---
layout: default
title: Features
parent: ITIP
nav_order: 2
---

# ITIP Features
{: .no_toc }

The capabilities ITIP delivers, grouped by functional component. Each capability carries a **milestone**; where it is already exercised by a role workflow, the **Usage scenario** column links to that page.

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

Milestones express prioritization and the engine-versus-application reality — not delivery dates. ITIP's application UI is in active design; several areas already have an implemented engine substrate in **[SIE Definition]({% link sie-definition.md %})**.

---

## Capabilities

| Functional component | Representative features | Milestone | Usage scenario |
|----------------------|-------------------------|-----------|----------------|
| Governance authoring | Create / edit Structures, Directives, Norms; Archetype-guided forms; approval workflow; lifecycle & Ascription version diff | Near-term | [Architect]({% link itip/usage-scenarios/architect.md %}), [Project Manager]({% link itip/usage-scenarios/project-manager.md %}) |
| Copilot-assisted authoring | Natural language → Directive / Norm; CEL Norm assistance; framework suggestion; impact analysis; compliance-gap detection | Mid-term | [Architect]({% link itip/usage-scenarios/architect.md %}) |
| Framework vocabulary & governance | Browse / compose framework stacks (TOGAF, ISO 25000-series, GDPR, NIS2, DORA); inspect framework Directives / Norms; regulatory coverage map; GSM → TOGAF / ArchiMate labels | Near-term | [Architect]({% link itip/usage-scenarios/architect.md %}), [Security Officer]({% link itip/usage-scenarios/security-officer.md %}), [Compliance Analyst]({% link itip/usage-scenarios/compliance-analyst.md %}) |
| Architecture discovery & visualization | Code-sourced inventory; dependency-chain extraction; reconciliation (authored vs code-sourced); topology & governance-overlay diagrams; impact / blast-radius | Near-term | [Developer]({% link itip/usage-scenarios/developer.md %}), [Operations]({% link itip/usage-scenarios/operations.md %}) |
| Views & diagram export | Multi-dimensional filtering; render UML / C4 / ArchiMate; export PlantUML and image (PNG / SVG / PDF) | Mid-term | [Developer]({% link itip/usage-scenarios/developer.md %}) |
| Continuous compliance & conformance | Conformance dashboard; drift detection & alerting; code-vs-governance conformance; SLO / SLA governance; compliance posture & audit-evidence reporting | Mid-term | [Operations]({% link itip/usage-scenarios/operations.md %}), [Compliance Analyst]({% link itip/usage-scenarios/compliance-analyst.md %}), [QA]({% link itip/usage-scenarios/qa-engineer.md %}), [Security Officer]({% link itip/usage-scenarios/security-officer.md %}) |
| Appraisal indicators (meta-governance) | Bilateral appraisal classes (AA, AC, DD, DN, NN) plus meta-governance zones (NA, NX); appraisal triggers, measures, and findings | Mid-term | [Compliance Analyst]({% link itip/usage-scenarios/compliance-analyst.md %}), [Security Officer]({% link itip/usage-scenarios/security-officer.md %}), [QA]({% link itip/usage-scenarios/qa-engineer.md %}) |
| Deliverable production | Generate ADRs, solution-design docs, component specs; API contracts & data schemas from Archetypes; IS-book generation with GSM provenance | Future | [Architect]({% link itip/usage-scenarios/architect.md %}), [Project Manager]({% link itip/usage-scenarios/project-manager.md %}) |
| External integrations | Jira (governance sync, gap → backlog); ServiceNow / CMDB; observability (Datadog / Grafana / Prometheus) ingest; Confluence; Backstage catalog | Future | [Developer]({% link itip/usage-scenarios/developer.md %}), [Operations]({% link itip/usage-scenarios/operations.md %}), [Project Manager]({% link itip/usage-scenarios/project-manager.md %}) |
| Role-based workspaces | Tailored workspaces for architect, developer, operations / SRE, project manager, security officer, compliance analyst, QA — each backed by a usage scenario | Future | [Architect]({% link itip/usage-scenarios/architect.md %}), [Developer]({% link itip/usage-scenarios/developer.md %}), [Project Manager]({% link itip/usage-scenarios/project-manager.md %}), [Operations]({% link itip/usage-scenarios/operations.md %}), [Security Officer]({% link itip/usage-scenarios/security-officer.md %}), [Compliance Analyst]({% link itip/usage-scenarios/compliance-analyst.md %}), [QA]({% link itip/usage-scenarios/qa-engineer.md %}) |
| Agentic governance substrate | GSM-as-MCP governed-context server; deterministic guardrail / offload API; agent identity & authorization as DNA; AI cost / efficiency governance; governed multi-agent workflows | Mid-term | — |

### Projected — not yet covered by a usage scenario

Several capability areas are on the roadmap but do not yet have a dedicated role page. They are projected and will gain usage scenarios as they mature:

- **Agentic governance substrate** — the platform's forward differentiator: GSM exposed as a governed Model Context Protocol (MCP) context server, a deterministic guardrail / offload API, agent identity and authorization expressed as DNA, and AI cost / efficiency governance.
- **The appraisal-indicator system by name** — the bilateral classes **AA, AC, DD, DN, NN** and the meta-governance zones **NA** and **NX**. The role pages touch appraisal results, but the indicator system itself has no dedicated scenario.
- **Central non-coding chatbot orchestration** — a single conversational entry point that routes governance questions and authoring across the platform.
- **Deliverable and IS-book generation** — assembling ADRs, solution-design documents, and a provenance-backed Information System book from governed definitions.
- **Confluence, CMDB, and Backstage integrations** — among the external integrations, these specific connectors are projected and not yet exercised by any role workflow.

---

For the concepts behind these capabilities, see the **[ITIP overview]({% link itip/index.md %})**; for hands-on workflows, the **[Usage Scenarios]({% link itip/usage-scenarios/index.md %})**.
