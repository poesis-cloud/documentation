---
layout: default
title: Features
nav_order: 2
---

# Features
{: .no_toc }

A portfolio-wide catalogue of Poesis product capabilities, grouped by product and then by functional component. Each capability carries a **milestone** that records how far it has progressed — from an implemented engine service to a research-tier idea. Where an ITIP capability is already covered by a hands-on role workflow, the table links to its **usage scenario**.

Think of this page as the bridge between the vision in the **[GSM Manifesto]({% link gsm-manifesto.md %})** and the practical, role-by-role **[ITIP Usage Scenarios]({% link itip/usage-scenarios/index.md %})**.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Milestone legend

- **Foundation** — implemented in the SIE engine today (real service code).
- **Near-term** — prioritized next (P0, feasibility now).
- **Mid-term** — planned (P1, feasibility next).
- **Future** — projected (P2–P3, later).
- **Exploratory** — research-tier; may evolve substantially or not ship.

Foundation marks capabilities already implemented in the SIE engine; ITIP application surfaces are in active design, so their milestones reflect prioritization, not delivery dates.

> **Reading the milestones.** These labels express prioritization and the current engine-versus-application reality — not delivery commitments. Only the **SIE engine** has real, running service code today. ITIP application surfaces and most analytics are in active design. No dates, metrics, or adopters are implied.

---

## GSM — the open standard

GSM (the Generative System Model) is not a product you deploy; it is the open systemic standard that every Poesis product implements. It fixes the shared governance grammar (DNA: Directive, Norm, Ascription), the eight primitives (Structure, Mechanism, Effector, Receptor, Interaction, Archetype, Directive, Norm), and the Archetype semantics that the engine and the domain applications all build on. Because GSM is the standard rather than a feature surface, it has no feature table of its own — its capabilities appear, realized, in the products below.

Read the **[GSM Manifesto]({% link gsm-manifesto.md %})** for what GSM is and why it must be open. GSM also has an academic-publication track (a paper and a book); that track is intentionally out of scope for this software-features catalogue.

---

## SIE — the engine

SIE (Systemic Intelligence Engine) is the engine that hosts GSM and enforces governance. It is the most mature part of the platform: the capabilities marked **Foundation** below are backed by real, running service code today. Everything else SIE offers builds outward from these foundational services toward a governance-intelligence layer that is still in design.

### Foundational services

The Definition Manager, the Operator, and the Blackboard are implemented engine services — the substrate every domain application is built on.

| Functional component | Representative features | Milestone | Usage scenario |
|----------------------|-------------------------|-----------|----------------|
| Definition Manager — GSM core | Author the 8 GSM primitives; DNA authoring (Directive / Norm / Ascription); Ascription lifecycle (DRAFT → … → RETIRED); Archetype schema validation | Foundation | — |
| Operator — rule runtime | Norm / Mechanism rule evaluation (Starlark sandbox); Effector / Receptor dispatch; closed-loop control | Foundation | — |
| Blackboard — collaborative sourcing | Contribution posting & validation; blackboard seal lifecycle (OPEN → SEALED → BYTE_STABLE); append-only audit ledger | Foundation | — |

### Governance intelligence (analytics)

These are projected engine capabilities — the analytical layer SIE will expose over the governed model. None are implemented yet.

| Functional component | Representative features | Milestone | Usage scenario |
|----------------------|-------------------------|-----------|----------------|
| Descriptive analytics | State monitoring & audit trail; structural observation (coupling, critical path); temporal observation (trend / drift detection) | Near-term | — |
| Diagnostic analytics | Causal attribution & root-cause; anomaly detection; constraint conflict / coherence / gap diagnostics | Mid-term | — |
| Predictive analytics | Forecasting; blast-radius & risk propagation; what-if / Norm simulation | Mid-term | — |
| Prescriptive analytics | Remediation recommendation; homeostasis (closed-loop); LLM-assisted DNA bootstrap | Near-term | — |
| Assurance & safety | Provenance & lineage; uncertainty / confidence; LLM-output assurance; automation guardrails | Near-term | — |
| Emergence & cross-domain inference | Emergence detection; code → business cross-domain impact | Exploratory | — |

### Environmental context and system presets

| Functional component | Representative features | Milestone | Usage scenario |
|----------------------|-------------------------|-----------|----------------|
| System presets | Regulatory / geopolitical / industry-standard presets; preset import & instantiation; preset composition & conflict detection | Near-term | — |

---

## ITIP — the IT domain application

ITIP (IT Intelligence Platform) translates GSM governance into IT vocabulary and workflows. It is the primary product surface and is in active design. The engine substrate for several areas already exists (the **Foundation** capabilities in SIE above), while the ITIP application UI itself is projected — so the milestones below reflect prioritization, not delivery.

Where an ITIP capability is already exercised by a role workflow, the **Usage scenario** column links to that role page.

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

Several ITIP capability areas are on the roadmap but do not yet have a dedicated role page. They are projected and will gain usage scenarios as they mature:

- **Agentic governance substrate** — the platform's forward differentiator: GSM exposed as a governed Model Context Protocol (MCP) context server, a deterministic guardrail / offload API, agent identity and authorization expressed as DNA, and AI cost / efficiency governance. No role page covers this yet.
- **The appraisal-indicator system by name** — the bilateral classes **AA, AC, DD, DN, NN** and the meta-governance zones **NA** and **NX**. The role pages touch appraisal results, but the indicator system itself has no dedicated scenario.
- **Central non-coding chatbot orchestration** — a single conversational entry point that routes governance questions and authoring across the platform.
- **Deliverable and IS-book generation** — assembling ADRs, solution-design documents, and a provenance-backed Information System book from governed definitions.
- **Confluence, CMDB, and Backstage integrations** — among the external integrations, these specific connectors are projected and not yet exercised by any role workflow.

---

## GSM Sourcer — the sourcing pipeline

The GSM Sourcer ingests external artifacts — code, API contracts, infrastructure, legal texts, and standards — and turns them into governed GSM definitions. Every sourced definition enters the model as a DRAFT, carrying its provenance. The collaborative contribution path is already implemented through the SIE Blackboard; the domain-specific source adapters are projected.

| Functional component | Representative features | Milestone | Usage scenario |
|----------------------|-------------------------|-----------|----------------|
| Core sourcing pipeline | Inventory & classification; deterministic + LLM extraction (hybrid); merge / deduplicate; GSM-JSON output with provenance (all output starts DRAFT) | Near-term | — |
| Collaborative contribution path | Blackboard contribution posting; confidence / provenance envelopes; sealed byte-stable streams | Foundation | — |
| IT-domain source adapters | Git repository (Java / Spring → Mechanism rules); API contracts (OpenAPI / gRPC / AsyncAPI); infrastructure (Helm / Dockerfile / Terraform) | Mid-term | — |
| Legal & regulatory adapters | EUR-Lex legislation (article → Directive, obligation → Norm); regulation-as-system modeling; multi-language | Future | — |
| Standards adapters | ISO/IEC, NIST CSF, CIS (SHALL / SHOULD → Directive, control → Norm); standard-as-system modeling | Future | — |

---

## How milestones are set

Milestones are not schedule promises. **Foundation** reflects capabilities that already exist as running engine code in SIE. **Near-term**, **Mid-term**, and **Future** reflect the priority (P0–P3) and feasibility recorded in the design-time backlog — ordered by what the platform can soundly build next, not by calendar date. **Exploratory** marks research-tier ideas that may change shape significantly or never ship.

For how these capabilities feel in practice, see the **[ITIP overview]({% link itip/index.md %})** and the role-by-role **[Usage Scenarios]({% link itip/usage-scenarios/index.md %})**.
