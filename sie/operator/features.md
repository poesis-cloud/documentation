---
layout: default
title: Features
parent: Operator
grand_parent: SIE
nav_order: 1
---

# Operator Features
{: .no_toc }

Capability catalogue for the Operator, grouped by functional component.

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
| GSM Norms evaluation API | Evaluate machine-evaluable Norms (CEL) against observed state — governance as a control loop | Foundation |
| GSM Mechanisms execution API | Execute governed Mechanisms; five deterministic phases — resolve, type-check against Archetype schemas, evaluate, verdict, dispatch | Foundation |
| Rule runtime & sandbox | Starlark rule evaluation in a step-limited sandbox — no ambient authority, no side effects, reproducible verdicts | Foundation |
| Effector / Receptor dispatch | Typed effect dispatch and closed-loop control; effectors and receptors derived from the rule code itself | Foundation |
