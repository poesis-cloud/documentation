---
layout: default
title: SAFe as the agentic harness
parent: SAFe Agentic Framework
nav_order: 1
---

# SAFe, run by agents, as the harness that makes agentic delivery trustworthy
{: .no_toc }

One idea carries the whole framework.

- **AI runs on intuition — exactly like we do.** An agent is a probabilistic guesser: brilliant, biased, predicting the next move from learned patterns. So is a person. Neither is, at bottom, a logician.
- **Methods are how intuition becomes reliable.** The scientific method, peer review, Scrum, SAFe — each is a rational and empirist *cognitive harness* that pushes a biased mind's output through evidence, checks, and sequence until it comes out trustworthy. *Intuition proposes; the method disposes.*
- **Agents need the same harness — and human methods fit them perfectly,** because those methods were engineered to tame the same probabilistic biases in us. You don't make an agent trustworthy by waiting for a smarter model; you make it **implement a method.**
- **A published standard is the strongest harness of all** — the AI already knows it, complies with it, and reasons in its vocabulary with no retraining. The method becomes a contract between human and machine.
- **A multi-layer harness governs every altitude** — divide & conquer only becomes *trustworthy* when every level of the work is bounded and checked. Most methods harness a single layer: Scrum governs the team, ITIL operations, TOGAF architecture. **SAFe governs all of them, from portfolio strategy to a merged commit.** The portfolio layer catches the wrong bet before it is funded; the program layer catches the wrong architecture before it is built; the iteration layer catches the wrong code before it ships. The probabilistic engine isn't filtered once — it is filtered at every level, each checkpoint owned by a human. That is the only harness that matches the full depth of the work.

That is what this is: **a method, run by agents, as the harness that makes agentic delivery trustworthy.** The method it runs is **SAFe** — but you don't have to *be* a SAFe organization to get the harness. Three properties make it work:

1. **Local-first** — the agent loop runs on each developer's machine, in the IDE, against the real working tree. Your code and secrets never leave; only the artifacts you commit sync out.
2. **Governed** — a portfolio → program → iteration hierarchy of role agents, with a human ★ gate at every layer. Not a flat swarm — an org chart with authority.
3. **Sovereign** — work state lives in your own files and git history (the event log), not a vendor's cloud. Nothing is trapped in a session.

Three orchestrators, one per SAFe layer, run the show — dispatched from a single entry point, `@vmo-orchestrator`:

```mermaid
flowchart LR
    CS(["Central Supervisor — the human<br/>value authority · owns every ★ gate"])

    subgraph FW["SAFe Agentic Framework — in your IDE (VS Code + Copilot)"]
      direction TB
      subgraph PORT["Portfolio layer · @vmo-orchestrator"]
        direction LR
        VMO{{"@vmo-orchestrator"}}
        ELBC["Epic Lean Business Case<br/>Agents: BO · EA · Sec · RAI"]
        AV["Architectural Vision<br/>Agents: EA · BO"]
        SPR["Strategic Portfolio Review<br/>Agents: BO · EA"]
        PB["Participatory Budgeting<br/>Agents: BO · EA"]
        PS["Portfolio Sync<br/>Agents: VMO + Epic owners"]
      end
      subgraph PROG["Program / ART layer · @rte-orchestrator"]
        direction LR
        RTE{{"@rte-orchestrator"}}
        FBR["Feature Backlog Refinement<br/>Agents: PM · Arch · Dev · QA · UX · Sec"]
        ARE["Architectural Runway Extension<br/>Agents: SA · Sec · DevOps · Dev"]
        PIP["PI Planning<br/>Agents: the ART"]
        SD["System Demo<br/>Agents: the ART"]
        ASY["ART Sync<br/>Agents: Arch + leads"]
        IA["Inspect and Adapt<br/>Agents: the ART"]
      end
      subgraph ITER["Team / Iteration layer · @sm-orchestrator"]
        direction LR
        SM{{"@sm-orchestrator"}}
        IP["Iteration Planning<br/>Agents: PO + pairs"]
        SBR["Story Backlog Refinement<br/>Agents: PO"]
        PAIR["Pair micro-cycle<br/>Agents: Dev · Dev · Sec"]
        VS["Verification and Sign-off<br/>Agents: QA · Sec"]
        DSR["Daily · Review · Retro<br/>Agents: the team"]
      end
      FSL[("local filesystem blackboard<br/>portfolio artifacts in Markdown")]
    end

    subgraph CENTRAL["Central systems — all synced from the git host"]
      direction TB
      GH["Git host — GitHub / GitLab<br/>boards · issues · artifact files"]
      JIRA["Ticketing — Jira<br/>SAFe Epics · Features · Stories · PIs"]
      CONF["Knowledge base — Confluence<br/>ADRs · PRDs · reports"]
      GH -->|"tickets"| JIRA
      GH -->|"knowledge"| CONF
    end

    CS ==>|"use case: strategic intent to governed delivery"| VMO
    VMO -.->|"dispatch · approved Epic to demoed Features"| RTE
    RTE -.->|"dispatch · committed Feature to merged Stories"| SM
    VMO -->|"returns ★ Epic gates"| CS
    RTE -->|"returns ★ Architecture · Demo · PR gates"| CS
    SM -->|"returns ★ Story · PR-packet gates"| CS
    VMO --> FSL
    RTE --> FSL
    SM --> FSL
    FSL -->|"sync · push/pull — the only external link"| GH

    classDef orch fill:#10b981,stroke:#065f46,color:#ffffff;
    classDef fs fill:#e0e7ff,stroke:#6366f1,color:#1e1b4b;
    classDef ext fill:#fde68a,stroke:#b45309,color:#3f2d00;
    class VMO,RTE,SM orch
    class FSL fs
    class GH,JIRA,CONF ext
```

*Each orchestrator is an entry point carrying your use case for its layer, and **returns that layer's ★ gates to you**. The framework's only external link is the git host — Jira and Confluence sync from there. The full model is on the **[Distributed Agentic SAFe]({% link safe-agentic-framework/distributed-agentic-safe.md %})** page.*
