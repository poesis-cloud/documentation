---
layout: default
title: Features
parent: Web Application
grand_parent: ITIP
nav_order: 2
redirect_from:
  - /itip/features/
---

# Web Application Features
{: .no_toc }

The Web Application's capabilities, grouped by functional component. Each section is one component of the product; the entries under it are the capabilities it provides. ITIP is in active design.

Each capability carries the ITIP **version** that delivers it: **v1** is the 1.0 (GA) scope; **v2** is the 1.x scope — see **[Milestones & Versions]({% link milestones.md %})** for the canonical version semantics and the delivery clause.

## Published feature catalogue

The product's published features on [poesis.cloud](https://poesis.cloud/solutions/itip/products/web-application) map onto the functional components below:

| Published feature | Functional component(s) |
|-------------------|-------------------------|
| IT artifact factory | [Deliverables](#deliverables) |
| IT compliance evaluation | [Evaluation](#evaluation) |
| IT impact simulation | [Simulation](#simulation) |
| GSM Definitions truth sourcing management | [Truth Sourcing](#truth-sourcing), [Review](#review) |
| GSM Definitions management | [Definition](#definition), [Lenses](#lenses), [Overview](#overview) |
| GSM Frameworks management | [Frameworks](#frameworks) |
| Role-based workspaces | [Admin](#admin), role-specific [Usage Scenarios]({% link itip/web-application/usage-scenarios/index.md %}) |

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

Governance posture at a glance.

| Capability | What it does | Version |
|------------|--------------|---------|
| Dashboard | Governance posture overview: definition counts, evaluation health, and recent changes | v2 |
| Activity | Chronological activity log / audit feed of governance events | v2 |

## Definition

The authoring core — create and manage the eight GSM primitives and drive the Ascription lifecycle.

| Capability | What it does | Version |
|------------|--------------|---------|
| Dashboard | Definition activity and health overview | v2 |
| Registry & Inventory | Browse, search, and filter every governed definition | v1 |
| Structures | Create and inspect **Structures** (systems, services, teams, platform components) | v1 |
| Archetypes | Create and inspect **Archetypes** — JSON-Schema-typed domain schemas | v1 |
| Directives | Author **Directives** in the Governance Authoring Workspace; view a Directive's Norms, history, and impact | v1 |
| Norms | Author and inspect **Norms** (CEL assertions) | v1 |
| Mechanisms | Author and inspect **Mechanisms** (Starlark rules) | v1 |
| Interactions | Wire and inspect **Interactions** (Effector ↔ Receptor coupling) | v1 |
| Ascription lifecycle | Bring a definition under governance, diff versions, and drive status transitions (DRAFT → … → RETIRED) | v1 |

## Evaluation

Appraisal of the governed model — the bilateral appraisal-indicator system, organized by class and zone, plus regulatory compliance views.

| Capability | What it does | Version |
|------------|--------------|---------|
| Dashboard | Aggregate appraisal posture across all indicator classes | v2 |
| Findings | Browse findings, overall and per bilateral class | v2 |
| AA · Source Fidelity | Ascription ↔ Ascription — sourced definitions stay faithful to their source | v2 |
| AC · Comitology Compliance | Ascription ↔ Comitology — changes followed the required decision procedure | v2 |
| DD · Directive Coherence | Directive ↔ Directive — Directives are mutually coherent | v2 |
| DN · Operationalization Integrity | Directive ↔ Norm — every Directive is properly operationalized into Norms | v2 |
| NN · Norm Coherence | Norm ↔ Norm — Norms are mutually coherent, with no conflicts | v2 |
| NA · Definition Compliance | Norm ↔ Ascription — in both the meta-governance and governance zones | v2 |
| NX · Execution Compliance | Norm ↔ eXecution — in both the meta-governance and governance zones | v2 |
| Adherence matrix | Regulatory adherence matrix across frameworks and Structures | v2 |
| Conformance | Conformance dashboard — drift of reality against governed intent | v2 |

## Frameworks

Browse and compose sourced governance frameworks.

| Capability | What it does | Version |
|------------|--------------|---------|
| Catalog | Browse available frameworks — GDPR, NIS2, ISO 25000 (SQuaRE), TOGAF 9.2, SCAP, the ITIP framework, and org frameworks such as ACME Corp | v1 |
| Framework detail | Inspect a framework's Directives, Norms, and vocabulary | v1 |
| Stack Composer | Compose multiple frameworks into one coherent governance stack | v1 |

## Lenses

Saved, multi-dimensional views over the governed model.

| Capability | What it does | Version |
|------------|--------------|---------|
| Browse | Browse saved lenses (named, filtered views) | v2 |
| Edit Lens | Create and edit a lens — multi-dimensional filters over the model | v2 |
| Diagram | Render a lens as a diagram (topology / governance overlay) | v2 |

## Simulation

Explore the consequences of a change before committing it.

| Capability | What it does | Version |
|------------|--------------|---------|
| Impact Analysis | Cascade / blast-radius analysis across dependent definitions | v2 |

## Review

The human governance gates — the comitology of approving change.

| Capability | What it does | Version |
|------------|--------------|---------|
| Review Board | Governance approvals board for pending lifecycle transitions | v2 |
| Sessions | Conduct a governance review session | v2 |
| History | Past review decisions and their rationale | v2 |

## Truth Sourcing

Connect external reality and keep the governed model in sync.

| Capability | What it does | Version |
|------------|--------------|---------|
| Sources | Manage connected sources (repositories, API contracts, infrastructure) | v1 |
| Source detail | Inspect a single source and what it contributes | v1 |
| Sync Jobs | Track sourcing / sync runs and their outcomes | v1 |

## Deliverables

Generate governed artifacts from definitions.

| Capability | What it does | Version |
|------------|--------------|---------|
| Templates | Catalog of deliverable templates (the artifact catalog) | v1 |
| Template Editor | Author and edit deliverable templates | v1 |
| Generated & Jobs | Generated deliverables and the generation jobs that produce them | v1 |

## Admin

| Capability | What it does | Version |
|------------|--------------|---------|
| Users | Users, roles, and permissions | v1 |
| Integrations | External-system integration settings | v1 |

## Guided Workflows

End-to-end walkthroughs that thread several capability areas together. They map onto the role-based **[Usage Scenarios]({% link itip/web-application/usage-scenarios/index.md %})**.

| Workflow | Threads together | Role | Version |
|----------|------------------|------|---------|
| Architect: Governance Authoring & Impact Analysis | Definition → Simulation | [Architect]({% link itip/web-application/usage-scenarios/architect.md %}) | v2 |
| Security Officer: Framework Stack Composition | Frameworks → Evaluation | [Security Officer]({% link itip/web-application/usage-scenarios/security-officer.md %}) | v2 |
| Governance Review Ceremony | Review → Definition | [Project Manager]({% link itip/web-application/usage-scenarios/project-manager.md %}) | v2 |
| Evaluation Status Transition | Evaluation → Definition | [Operations]({% link itip/web-application/usage-scenarios/operations.md %}), [QA]({% link itip/web-application/usage-scenarios/qa-engineer.md %}) | v2 |

---

For the concepts behind these capabilities, see the **[ITIP overview]({% link itip/web-application/index.md %})**; for hands-on, role-by-role workflows, the **[Usage Scenarios]({% link itip/web-application/usage-scenarios/index.md %})**.
