---
layout: default
title: Agentic Harness
parent: SAF
nav_order: 2
has_children: true
redirect_from:
  - /safe-agentic-framework/safe-as-the-harness/
---

# Agentic Harness

{: .no_toc }

The **Agentic Harness** is the deterministic execution core of the Systemic Agentic Framework: it resolves workflows, steps, models, and agent session context (instructions and skills — injected at session open), checks step conditions, authorization, and artifacts, and journals all of it — deterministically, from persisted state and validated configuration only. Probabilistic agents propose; the harness verifies.

The harness core is fully **methodology- and host-agnostic**. It knows nothing about SAFe or any particular agent host: the embedding framework and the data plane are supplied as environment-anchored paths (`FRAMEWORK_DIR`, `FRAMEWORK_WORKSPACE_DIR`), and host-specific bindings live in separate adapter specifications (VS Code / GitHub Copilot Chat today). The same workflows run unchanged in an IDE, a CI runner, or another agent host.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## What it does

- **Workflow & step resolution** — workflow and step graphs are resolved deterministically from plain files; the next orchestration action (dispatch, halt, done) is computed, never guessed.
- **Session context injection** — the skills and instructions a step needs are resolved and injected into the agent's context at session open.
- **LLM resolution** — the model backing each step is resolved from declared model profiles: deterministic tier and capability-score routing, no hard-wired vendor.
- **Condition checks & authorization** — pre, invariant, and post conditions gate every step; an access-control list decides which agent may execute it.
- **Artifact validation** — agents stage writes in the working tree; the harness validates the staged bytes against the framework's JSON Schema artifact contracts before commit. One validated write = one commit, attributed to the acting session. Invalid bytes never land.
- **Journaling** — every step execution appends to a session ledger, so the delivery history is an auditable event log, not a chat scrollback.

See **[Features]({% link saf/agentic-harness/features.md %})** for the capability catalogue.

## Using the CLI

The harness is a stable CLI over plain files — `harness.py` in the [`saf-agentic-harness`](https://github.com/poesis-cloud/saf-agentic-harness) repository. Global options (`--portfolio-root`, `--strict`, `--json`) come before the command:

```bash
# STATE — validate Epic/Feature/Story artifacts (FSM, linkage, schema, gates, derived fields)
python3 harness.py --portfolio-root /path/to/portfolio \
  check-artifact --unit-id <unit-id>

# DRIVE — resolve the next orchestration action (dispatch | halt | done)
python3 harness.py orchestrate --workflow <workflow> --unit <unit-id>

# CONDITIONS — evaluate one step's conditions and append the session ledger line
python3 harness.py check-step --orchestration <workflow> --step <step-id>
```

Point the harness at the framework application with `FRAMEWORK_DIR` and at the data plane with `FRAMEWORK_WORKSPACE_DIR`:

```bash
FRAMEWORK_DIR=/abs/path/to/saf-agentic-organization
FRAMEWORK_WORKSPACE_DIR=../saf-agentic-workspace
```

## In the SAF solution

| Product | Role |
|---|---|
| **Agentic Harness** (this product) | the deterministic execution engine — methodology- and host-agnostic |
| [SAFe Agentic Organization]({% link saf/safe-agentic-organization/index.md %}) | the SAFe-shaped framework application the harness executes |
| [Agentic Workspace]({% link saf/agentic-workspace/index.md %}) | the shared data plane the harness checks and commits into |

The canonical harness-core specification — terminology, invariants, the eleven-function contract, design, and implementation — lives in the repository at [`def/core/spec.md`](https://github.com/poesis-cloud/saf-agentic-harness/blob/main/def/core/spec.md); each host binding has its own specification under `def/adapter/<host>/spec.md`.
