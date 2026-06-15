---
layout: default
title: Getting Started
parent: ITIP
nav_order: 1
---

# Getting Started — Your First Governed Definition
{: .no_toc }

This tutorial walks you through authoring your first governed definition in ITIP, end to end. You'll express one real governance intent — *the payment gateway must stay available* — and turn it into something ITIP can continuously enforce.

By the end you will have created a **Directive**, operationalized it with a **Norm**, and moved both through a governed lifecycle as **Ascriptions**. You don't need any prior knowledge of GSM or DNA — we introduce each idea exactly when you need it, and link to [General Usage]({% link itip/general-usage.md %}) whenever you want more depth.

<details open markdown="block">
  <summary>Table of contents</summary>
  {: .text-delta }
- TOC
{:toc}
</details>

---

## What you'll build

A complete, minimal governance chain for a single service:

```
Directive    the architecture board requires the payment gateway to be reliable
   │
   ▼
Norm         availability must be at least 99.9%, sustained over 30 days
   │
   ▼
Ascription   the governed, versioned snapshot of each — moving DRAFT → ACTIVE
```

This is the smallest end-to-end slice of ITIP: a strategic intent, a measurable constraint, and the governed lifecycle that makes both auditable.

## Before you start

- Access to an ITIP workspace with author permissions for governance content.
- A structure to govern. This tutorial uses a service called `payment-gateway`; if your workspace already has one, use it — otherwise any service-type structure works.

> This is a design-phase walkthrough. The navigation paths and form fields below describe ITIP's intended authoring flow; exact labels may change as the interface is built. There are no screenshots yet — follow the steps and read the "you'll see" cues.

---

## Step 1 — Author the Directive

A **Directive** is a single governance statement: a governing entity declares that a governed entity *must* achieve or avoid something along one dimension. It carries no thresholds — just the intent.

1. Open the **Governance** workspace and choose **Directives → New Directive**.
2. Fill in the structured form:
   - **Governing structure**: `enterprise-architecture-board`
   - **Modal**: `MUST`
   - **Verb**: `ENSURE`
   - **Qualifier** (the dimension being governed): `ProductReliability`
   - **Governed structure**: `payment-gateway`
3. Submit the Directive.

You've just declared:

```
enterprise-architecture-board MUST ENSURE ProductReliability ON payment-gateway
```

Read it back: *"The architecture board declares that the payment gateway must ensure product reliability."* There's no number yet — a Directive opens the governance scope; the threshold comes next.

> **Tip.** ITIP's Copilot can draft this for you: describe the intent in plain language ("the payment gateway must stay reliable") and it suggests the structured Directive. You confirm the fields before submitting.

For the full Directive grammar — every modal, verb, and qualifier — see [General Usage]({% link itip/general-usage.md %}).

---

## Step 2 — Operationalize it with a Norm

A **Norm** makes a Directive measurable. Where the Directive said *ensure reliability*, the Norm says *exactly how reliable, measured how, over what window*.

1. Go to **Governance → Norms → New Norm**.
2. Select the **governed structure**: `payment-gateway`. You'll see only structures that already have an active Directive — which is why Step 1 came first.
3. Select the **qualifier**: `ProductReliability` — the same dimension your Directive opened.
4. Write the **applicability** (when the Norm applies). For production only:
   - `ServiceTelemetry.environment == "production"`
5. Write the **assertion** (the condition that must hold):
   - `ServiceTelemetry.availability30d >= 0.999`
6. Choose the **tolerance mode**: `SUSTAINED` over a 30-day window — availability targets allow brief dips inside an error budget.
7. Submit the Norm.

You've now expressed:

```
payment-gateway ON ProductReliability:
  WHEN ServiceTelemetry.environment == "production"
  ASSERT ServiceTelemetry.availability30d >= 0.999
  (SUSTAINED over P30D)
```

Your strategic intent is now a machine-evaluable constraint. Notice the chain: the Norm could only attach because a Directive already governed `payment-gateway` on `ProductReliability`. Governance in ITIP is intentional — every constraint traces back to a declared intent.

> **Tip.** Copilot can help here too: describe the requirement in plain language ("99.9% availability over 30 days in production") and it suggests the assertion and tolerance mode. The tolerance modes (`INSTANTANEOUS`, `AGGREGATED`, `SUSTAINED`) are explained in [General Usage]({% link itip/general-usage.md %}).

---

## Step 3 — Move it through its lifecycle (the Ascription)

Everything you just created is carried by an **Ascription** — the governed, versioned snapshot that binds a definition to its subject and tracks its state. You didn't create Ascriptions explicitly; ITIP created one for the Directive and one for the Norm the moment you submitted each.

Every Ascription starts in `DRAFT` and advances through a governed lifecycle:

```
DRAFT → PROPOSED → APPROVED → ACTIVE → … → RETIRED
```

To make your governance take effect:

1. Open your Directive (it's in `DRAFT`) and choose **Submit**. It moves to `PROPOSED`.
2. A governance approver reviews it and **Approves** it. It moves to `APPROVED`, and a version number is assigned.
3. **Activate** it. It moves to `ACTIVE`.
4. Repeat the same three transitions for your Norm.

Once the Norm is `ACTIVE`, ITIP evaluates it continuously against the payment gateway's telemetry. If sustained 30-day availability drops below 99.9% in production, the Norm reports a violation — which is exactly the reliability the architecture board asked for in Step 1.

> **You can't edit an `ACTIVE` definition in place.** To change it later, you create a *new* Ascription of the same definition; it runs through the lifecycle again, and the previous version is retired when the new one activates. That's what makes every change auditable — the full lifecycle and its rules are covered in [Rules]({% link itip/rules.md %}).

---

## What you did

In three steps you took a governance intent from idea to continuously-enforced constraint:

- a **Directive** captured the strategic intent (reliability on the payment gateway),
- a **Norm** made it measurable (≥ 99.9% availability, sustained over 30 days),
- an **Ascription** carried each through a governed, versioned lifecycle.

That is the core loop of ITIP. Every other kind of governance — security, compliance, performance, data quality — is authored exactly the same way.

## Where to next

- **[General Usage]({% link itip/general-usage.md %})** — the full DNA grammar, tolerance modes, and how to compose Framework stacks.
- **[Usage Scenarios]({% link itip/usage-scenarios/index.md %})** — how your specific role uses ITIP day to day.
- **[Rules]({% link itip/rules.md %})** — the lifecycle and governance rules that apply to everything you author.
- **[ITIP Overview]({% link itip/index.md %})** — the concepts and the bigger picture behind what you just built.
