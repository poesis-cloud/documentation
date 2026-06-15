---
layout: default
title: Features
parent: ITIP
nav_order: 2
---

# ITIP Features
{: .no_toc }

ITIP's capabilities, organized exactly as the application's left-hand **menu** groups them. Each section below is a functional component of the product; the features under it are taken from the ITIP interface wireframes (the `v1` and `experimental` design mockups). The UI is in active design, so these describe intended screens, not delivered software.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

The landing area — governance posture at a glance.

| Capability | What it does |
|------------|--------------|
| Dashboard | Governance posture overview: definition counts, evaluation health, and recent changes |
| Activity | Chronological activity log / audit feed of governance events |

## Definition

The authoring core — create and manage the eight GSM primitives and drive the Ascription lifecycle.

| Capability | What it does |
|------------|--------------|
| Dashboard | Definition activity and health overview |
| Registry & Inventory | Browse, search, and filter every governed definition |
| Structures | Create and inspect **Structures** (systems, services, teams, platform components) |
| Archetypes | Create and inspect **Archetypes** — JSON-Schema-typed domain schemas |
| Directives | Author **Directives** in the Governance Authoring Workspace; view a Directive's Norms, history, and impact |
| Norms | Author and inspect **Norms** (CEL assertions) |
| Mechanisms | Author and inspect **Mechanisms** (Starlark rules) |
| Interactions | Wire and inspect **Interactions** (Effector ↔ Receptor coupling) |
| Ascription lifecycle | Bring a definition under governance, diff versions, and drive status transitions (DRAFT → … → RETIRED) |

## Evaluation

Appraisal of the governed model — the bilateral appraisal-indicator system, organized by class and zone, plus regulatory compliance views.

| Capability | What it does |
|------------|--------------|
| Dashboard | Aggregate appraisal posture across all indicator classes |
| Findings | Browse findings, overall and per bilateral class |
| AA · Source Fidelity | Ascription ↔ Ascription — sourced definitions stay faithful to their source |
| AC · Comitology Compliance | Ascription ↔ Comitology — changes followed the required decision procedure |
| DD · Directive Coherence | Directive ↔ Directive — Directives are mutually coherent |
| DN · Operationalization Integrity | Directive ↔ Norm — every Directive is properly operationalized into Norms |
| NN · Norm Coherence | Norm ↔ Norm — Norms are mutually coherent, with no conflicts |
| NA · Definition Compliance | Norm ↔ Ascription — in both the meta-governance and governance zones |
| NX · Execution Compliance | Norm ↔ eXecution — in both the meta-governance and governance zones |
| Adherence matrix | Regulatory adherence matrix across frameworks and Structures |
| Conformance | Conformance dashboard — drift of reality against governed intent |

## Frameworks

Browse and compose sourced governance frameworks.

| Capability | What it does |
|------------|--------------|
| Catalog | Browse available frameworks — GDPR, NIS2, ISO 25000 (SQuaRE), TOGAF 9.2, SCAP, the ITIP framework, and org frameworks such as ACME Corp |
| Framework detail | Inspect a framework's Directives, Norms, and vocabulary |
| Stack Composer | Compose multiple frameworks into one coherent governance stack |

## Lenses

Saved, multi-dimensional views over the governed model.

| Capability | What it does |
|------------|--------------|
| Browse | Browse saved lenses (named, filtered views) |
| Edit Lens | Create and edit a lens — multi-dimensional filters over the model |
| Diagram | Render a lens as a diagram (topology / governance overlay) |

## Simulation

Explore the consequences of a change before committing it.

| Capability | What it does |
|------------|--------------|
| Impact Analysis | Cascade / blast-radius analysis across dependent definitions |

## Review

The human governance gates — the comitology of approving change.

| Capability | What it does |
|------------|--------------|
| Review Board | Governance approvals board for pending lifecycle transitions |
| Sessions | Conduct a governance review session |
| History | Past review decisions and their rationale |

## Truth Sourcing

Connect external reality and keep the governed model in sync.

| Capability | What it does |
|------------|--------------|
| Sources | Manage connected sources (repositories, API contracts, infrastructure) |
| Source detail | Inspect a single source and what it contributes |
| Sync Jobs | Track sourcing / sync runs and their outcomes |

## Deliverables

Generate governed artifacts from definitions. *(Called **Artifactory** in the `v1` wireframes.)*

| Capability | What it does |
|------------|--------------|
| Templates | Catalog of deliverable templates (the artifact catalog) |
| Template Editor | Author and edit deliverable templates |
| Generated & Jobs | Generated deliverables and the generation jobs that produce them |

## Admin

| Capability | What it does |
|------------|--------------|
| Users | Users, roles, and permissions |
| Integrations | External-system integration settings |

## Guided Workflows

End-to-end walkthroughs that thread several menu areas together. They map onto the role-based **[Usage Scenarios]({% link itip/usage-scenarios/index.md %})**.

| Workflow | Threads together | Role |
|----------|------------------|------|
| Architect: Governance Authoring & Impact Analysis | Definition → Simulation | [Architect]({% link itip/usage-scenarios/architect.md %}) |
| Security Officer: Framework Stack Composition | Frameworks → Evaluation | [Security Officer]({% link itip/usage-scenarios/security-officer.md %}) |
| Governance Review Ceremony | Review → Definition | [Project Manager]({% link itip/usage-scenarios/project-manager.md %}) |
| Evaluation Status Transition | Evaluation → Definition | [Operations]({% link itip/usage-scenarios/operations.md %}), [QA]({% link itip/usage-scenarios/qa-engineer.md %}) |

---

For the concepts behind these capabilities, see the **[ITIP overview]({% link itip/index.md %})**; for hands-on, role-by-role workflows, the **[Usage Scenarios]({% link itip/usage-scenarios/index.md %})**.
