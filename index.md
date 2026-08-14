---
layout: default
title: Home
nav_exclude: true
permalink: /
---

# Poesis Documentation

Welcome to the user documentation for **Poesis** products.

Poesis builds products that bring **systemic governance** to organizations — replacing fragmented, manual, and permanently outdated governance practices with a continuous, machine-enforceable governance fabric.

---

## Solutions

Poesis is layered: the **GSM** standard, the **SIE** engine that implements it, domain applications built on top such as **ITIP** for the IT domain, and **SAF** to build them. Each solution below groups the products it ships.

### [ITIP — IT Intelligence Platform]({% link itip/index.md %})

The first domain application built on SIE. ITIP is where all IT profiles converge — architects, developers, ops engineers, project managers, security officers, compliance analysts — to define, govern, and visualize the IT landscape through a single governed source of truth.

- **[Web Application]({% link itip/web-application/index.md %})** — the application every IT profile works in
  - [Overview]({% link itip/web-application/index.md %}) — the THINK gap, the Definition–Execution–Observation triad, and DNA governance grammar
  - [General Usage]({% link itip/web-application/general-usage.md %}) — Directives, Norms, Ascriptions, and Frameworks in practice
  - [Usage Scenarios]({% link itip/web-application/usage-scenarios/index.md %}) — role-specific workflows per IT profile
  - [Features]({% link itip/web-application/features.md %}) — the capability catalogue with milestones
  - [Rules]({% link itip/web-application/rules.md %}) — governance rules every user must know
- **[Definition Blackboard Code Sourcer]({% link itip/definition-blackboard-code-sourcer/index.md %})** — client pipeline that sources IT artifacts — code, API contracts, infrastructure — into governed GSM definitions on the Definition Blackboard Manager. *Documentation in construction.*
  - [Features]({% link itip/definition-blackboard-code-sourcer/features.md %}) — the capability catalogue with milestones

### [SIE — Systemic Intelligence Engine]({% link sie/index.md %})

The reference implementation of GSM: the engine that hosts governed definitions, enforces their lifecycle, evaluates Norms, and executes Mechanisms.

- **[Definition Manager]({% link sie/definition-manager/index.md %})** — the authoritative API, lifecycle enforcer, and store of every governed GSM Definition. *Documentation in construction.*
  - [Features]({% link sie/definition-manager/features.md %}) — the capability catalogue with milestones
- **[Operator]({% link sie/operator/index.md %})** — the GSM Definition runtime for Norms and Mechanisms. *Documentation in construction.*
- **[Definition Blackboard Manager]({% link sie/definition-blackboard-manager/index.md %})** — collaborative definition-sourcing service with a sealed, byte-stable contribution lifecycle and an append-only audit ledger. *Documentation in construction.*
  - [Features]({% link sie/definition-blackboard-manager/features.md %}) — the capability catalogue with milestones

### [GSM — the standard]({% link gsm/index.md %})

The **Generative System Model (GSM)** is the vendor-neutral standard for the THINK side of IT — *defining and governing* systems, the way OpenTelemetry standardized *observing* them. It turns governance from prose that *describes* systems into definitions that *generate* them, and every Poesis product implements it. GSM is a pre-1.0 working draft, source-available under BUSL-1.1 and developed as a candidate for contribution as an open standard.

- **Specifications** — eight primitives, DNA grammar, Archetyping, and the systemic lifecycle. *Publication pending — the specification document set is being finalized for release.*
- **[Frameworks]({% link gsm/frameworks/index.md %})** — domain, standard, and legal vocabularies sourced into GSM, ready to enforce. *Documentation in construction.*

### [SAF — Systemic Agentic Framework]({% link saf/index.md %})

The first **distributed agentic SAFe** engine — a governed, local-first, multi-agent way to *run SAFe*, today in VS Code / GitHub Copilot and portable to any host the harness adapts to next. Portfolio–program–iteration orchestration runs on your own machine, with a human gate at every layer; connected to the Poesis ecosystem, its agents build with full, governed knowledge of your organization.

- [Overview]({% link saf/index.md %}) — the vision, the model, and the Poesis ecosystem advantage
- [Quickstart]({% link saf/quickstart.md %}) — install and run your first orchestrated PR in under 30 minutes
- **[Agentic Harness]({% link saf/agentic-harness/index.md %})** — deterministic resolution, validation, and traceability that keep probabilistic agents on rails
- **[SAFe Agentic Organization]({% link saf/safe-agentic-organization/index.md %})** — orchestrators, layers, ceremonies, agents, and the filesystem ⇆ central-systems sync
- **[Agentic Workspace]({% link saf/agentic-workspace/index.md %})** — the shared remote workspace for agentic workflow artifacts. *Documentation in construction.*
