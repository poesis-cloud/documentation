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

## Products

Poesis is layered: the **GSM** standard, the **SIE** engine that implements it, and domain applications built on top, such as **ITIP** for the IT domain. Below are the products tracked in our delivery workflow, together with the GSM standard they all implement.

### GSM — the open standard

The **Generative System Model (GSM)** is the open standard for the THINK side of IT — *defining and governing* systems, the way OpenTelemetry standardized *observing* them. It turns governance from prose that *describes* systems into definitions that *generate* them, and every Poesis product implements it.

### [SIE Definition]({% link sie-definition.md %})

The engine that hosts GSM and enforces governance — Definition Manager, Operator rule runtime, and database. *Documentation in construction.*

- [Features]({% link sie-definition/features.md %}) — the SIE Definition capability catalogue with milestones

### [SIE Blackboard]({% link sie-blackboard.md %})

Collaborative definition-sourcing service with a sealed, byte-stable contribution lifecycle and an append-only audit ledger. *Documentation in construction.*

- [Features]({% link sie-blackboard/features.md %}) — the SIE Blackboard capability catalogue with milestones

### [ITIP — IT Intelligence Platform]({% link itip/index.md %})

The first domain application built on SIE. ITIP is where all IT profiles converge — architects, developers, ops engineers, project managers, security officers, compliance analysts — to define, govern, and visualize the IT landscape through a single governed source of truth.

- [Overview]({% link itip/index.md %}) — the THINK gap, the Definition–Execution–Observation triad, and DNA governance grammar
- [General Usage]({% link itip/general-usage.md %}) — Directives, Norms, Ascriptions, and Frameworks in practice
- [Usage Scenarios]({% link itip/usage-scenarios/index.md %}) — role-specific workflows per IT profile
- [Features]({% link itip/features.md %}) — the ITIP capability catalogue with milestones
- [Rules]({% link itip/rules.md %}) — governance rules every user must know

### [ITIP Blackboard Sourcer]({% link itip-blackboard-sourcer.md %})

Client pipeline that sources IT artifacts — code, API contracts, infrastructure — into governed GSM definitions on the SIE Blackboard. *Documentation in construction.*

- [Features]({% link itip-blackboard-sourcer/features.md %}) — the ITIP Blackboard Sourcer capability catalogue with milestones

### [SAFe Agentic Framework]({% link safe-agentic-framework.md %})

The first **distributed agentic SAFe** engine — a governed, local-first, multi-agent way to *run SAFe* in VS Code / GitHub Copilot. Portfolio–program–iteration orchestration runs on your own machine, with a human gate at every layer; connected to the Poesis ecosystem, its agents build with full, governed knowledge of your organization.

- [Overview]({% link safe-agentic-framework.md %}) — the vision, the model, and the Poesis ecosystem advantage
- [Distributed Agentic SAFe]({% link safe-agentic-framework/distributed-agentic-safe.md %}) — orchestrators, layers, ceremonies, agents, and the filesystem ⇆ central-systems sync
- [Quickstart]({% link safe-agentic-framework/quickstart.md %}) — install and run your first orchestrated PR in under 30 minutes
