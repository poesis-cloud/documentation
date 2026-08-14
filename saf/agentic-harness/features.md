---
layout: default
title: Features
parent: Agentic Harness
grand_parent: SAF
nav_order: 1
---

# Agentic Harness Features
{: .no_toc }

Capability catalogue for the Agentic Harness.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

{% include milestone_legend.md %}

---

## Capabilities

| Functional component | Representative features | Milestone |
|----------------------|-------------------------|-----------|
| Workflow & step resolution | Workflow and step graphs resolved deterministically from plain files; orchestration actions (dispatch / halt / done) computed from persisted state | Foundation |
| Skill and instruction prompt injection | Skills and instructions resolved and injected into the agent's session context at session open | Foundation |
| LLM resolution | Model tier + capability-score routing from declared model profiles — deterministic, host-agnostic, no hard-wired vendor | Foundation |
| Artifact validation | Staged bytes validated against JSON Schema artifact contracts before commit; one validated write = one commit; invalid bytes never land | Foundation |
| Agent authorization | Pre, invariant, and post conditions gate every step; access-control list decides which agent may execute it | Foundation |
| Logging | Session ledger appended on every step execution — an auditable event log of the delivery history | Foundation |
| Host adapters | VS Code / GitHub Copilot Chat binding today; further host bindings behind the same adapter contract | Near-term |
