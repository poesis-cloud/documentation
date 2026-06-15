---
layout: default
title: ITIP
nav_order: 3
has_children: true
---

# ITIP — IT Intelligence Platform

ITIP (IT Intelligence Platform) is a domain application for **defining and governing IT systems as integrated wholes**. It centralizes governance concerns — architecture, compliance, quality, operational constraints — in a single governed model, and continuously evaluates that model against reality.

This page explains the concepts behind ITIP. It assumes you have already chosen to evaluate the platform and want to understand how it works.

> **New to ITIP?** Start with the **[Getting Started]({% link itip/getting-started.md %})** tutorial — it walks you through authoring your first Directive, Norm, and Ascription end to end. Come back here when you want the concepts behind what you built.

---

## The THINK gap

Every IT organization runs three fundamental activities:

- **BUILD** — design, develop, and deliver systems (CI/CD, IDEs, source control, DevOps platforms).
- **RUN** — supervise, operate, and maintain them (observability, incident management, ITSM).
- **THINK** — govern, regulate, and align them.

BUILD and RUN have mature, automated toolchains. THINK — the activity that *aligns* BUILD and RUN — is typically handled by a patchwork of architecture wikis, compliance spreadsheets, and periodic review boards. The practical consequence is that the **definition** of what IT systems should be lives in scattered, manually maintained artifacts that drift from reality.

ITIP addresses the THINK activity directly: it provides a single, governed, machine-evaluable place to express what systems must be, and to check continuously whether they are.

---

## Definition, Execution, Observation

ITIP is organized around the relationship between three layers:

```
            ┌──────────────┐
            │    THINK     │
            │  Definition  │  ◄── ITIP lives here
            │  (ITIP/SIE)  │
            └──────┬───────┘
                   │
         ┌─────────┴─────────┐
         │                   │
         ▼                   ▼
  ┌──────────────┐   ┌──────────────┐
  │    BUILD     │   │     RUN      │
  │  Execution   │   │ Observation  │
  │  (CI/CD,     │   │ (Datadog,    │
  │   DevOps)    │   │  Grafana)    │
  └──────────────┘   └──────────────┘
```

**Definition is generative**: it tells BUILD *what to produce* and tells RUN *what to measure against*. When BUILD and RUN both reference the same governed definitions, they become coherent *with each other* rather than operating in isolation. ITIP owns the definition layer; code repositories, running services, and telemetry are downstream of the definitions that describe them.

---

## DNA: the governance grammar

ITIP is built on **SIE (Systemic Intelligence Engine)**, which implements the **Generative System Model (GSM)** — a formal model for defining and governing systems. At the heart of GSM is a governance grammar called **DNA**:

| Letter | Primitive | What it does |
|--------|-----------|--------------|
| **D** | Directive | A **strategic operational intent** — declares what a system *must* achieve or avoid. |
| **N** | Norm | A **tactical assertion and measure** — operationalizes a Directive into a machine-evaluable constraint. |
| **A** | Ascription | Binds a definition to its governed subject — the versioned, lifecycle-managed snapshot. |

DNA descends from strategy to measurement. A **Directive** sets the slow-changing intent; a **Norm** turns it into something machines can enforce; an **Ascription** versions every change. Every governed item — from an enterprise architecture principle to a single service's latency threshold — is expressed as DNA.

The grammar is precise, not metaphorical:

- A **Directive** reads: *"The architecture board MUST ENSURE availability OF the payment gateway."*
- A **Norm** reads: *"The payment gateway ON availability: ASSERT availability30d >= 0.999 (SUSTAINED over 30d)."*
- An **Ascription** binds these definitions to their subjects with a governed lifecycle (DRAFT → PROPOSED → APPROVED → ACTIVE → … → RETIRED).

[General Usage]({% link itip/general-usage.md %}) walks through each DNA primitive in detail with worked examples.

---

## Archetypes and Frameworks: where meaning comes from

GSM's core is deliberately small — eight primitives and the DNA grammar — but a grammar alone doesn't know what *reliability* or *GDPR Article 32* mean. That meaning comes from **Archetypes**: typed domain schemas that fix what each property means, its constraints, and its relationships, so the meaning travels with the type rather than living in someone's head.

Archetypes are grouped into **Frameworks** — established bodies of knowledge (TOGAF, ISO 25010, ISO 25012, GDPR, NIS2, DORA, SOC 2) *sourced into GSM*. A Framework brings ready-made Directives and Norms that encode the standard's requirements as governance you can enforce. Because every Framework speaks the same DNA, Frameworks compose into one coherent governance fabric instead of staying in separate silos.

[General Usage]({% link itip/general-usage.md %}) covers the Framework catalogue and how to compose Framework stacks in practice.

---

## IT systems are socio-technical systems

One insight shapes the whole model: **the system is not the code.** The decisions that matter — what a service does, how services interact, what "healthy" means, when something may change — are human governance decisions that precede and constrain the technical layer.

- A product owner, architect, or tech lead decides a service's purpose and boundary.
- Architects and developers define API contracts and integration topology before they are implemented.
- Ops engineers, compliance analysts, and business owners define the SLOs, SLAs, and thresholds that say what "healthy" means.
- Change boards, PR reviews, and deployment gates decide when the technical system may evolve.

When an incident happens, the technical failure is usually the symptom of a governance gap — a dependency nobody documented, a constraint nobody enforced, a change nobody assessed. ITIP treats the **definition** (the human governance decisions) as the generative source, and treats code, services, and telemetry as downstream artifacts. DNA is the practical lever: a machine-enforceable grammar for expressing human governance intent over technical systems.

---

## Where to next

- **[GSM Manifesto]({% link gsm-manifesto.md %})** — ITIP is built on GSM, an open standard for defining and governing systems.
- **[Getting Started]({% link itip/getting-started.md %})** — author your first Directive, Norm, and Ascription, step by step.
- **[General Usage]({% link itip/general-usage.md %})** — the DNA primitives and Frameworks in depth, with worked examples.
- **[Usage Scenarios]({% link itip/usage-scenarios/index.md %})** — role-specific workflows for each IT profile.
- **[Rules]({% link itip/rules.md %})** — the governance rules every user must know.
