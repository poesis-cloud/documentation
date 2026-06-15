# `_comsite/` — Marketing Capture (Staging)

This folder is a **staging design artifact** for a future, **separate** marketing
property (`poesis.cloud`). It is **not** part of the documentation site
(`docs.poesis.cloud`), and it is **excluded from the Jekyll build** via the
`exclude:` list in [`_config.yml`](../_config.yml).

## Why it exists

The documentation site follows the industry-standard split (Stripe, Datadog,
OpenTelemetry, Diátaxis): **documentation** stays neutral and task-first so it can
serve evaluators who are already in the door, while **marketing / capture** content —
hero messaging, competitive positioning, ROI, and CTAs — lives on a separate property.

When the ITIP docs were reframed to be neutral and task-first, the persuasion content
was moved here rather than deleted, so it is preserved and ready to seed the marketing
site when that property is built.

## What's here

- `landing.md` — a self-contained draft of the marketing landing / capture page:
  hero + CTA, the BUILD / RUN / THINK framing, a "problems we solve" pain list,
  competitive positioning ("how it's different"), the GSM-as-open-standard story
  (the OpenTelemetry analogy), the AI-economics pitch ("define once, regenerate
  forever for free"), a **Proof** section with `TODO` placeholders, and a closing CTA.

## Status and rules

- **Not wired to any site.** This is a content draft only — no layout, theme, routing,
  or deployment is attached.
- **Excluded from the docs build.** Nothing in this folder is published to
  `docs.poesis.cloud`.
- **Placeholders are intentional.** Proof points are marked `TODO`; do not publish
  fabricated cases, logos, metrics, or testimonials.
- **Not Jekyll-linked.** Because this folder targets a different property, its internal
  links are plain placeholders (`#TODO`), not Jekyll `{% link %}` tags.
