---
layout: default
title: Quickstart
parent: SAF
nav_order: 1
redirect_from:
  - /safe-agentic-framework/quickstart/
---

# Quickstart — SAFe Agentic Framework

{: .no_toc }

This guide takes you from a fresh install to your first successful orchestrated PR.
Target: **under 30 minutes**.

## Table of contents

{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Prerequisites

Before you start, you need:

1. **VS Code** (1.90 or later) with the **GitHub Copilot** extension installed and signed in.
2. **Git** (any recent version).
3. The following **external prerequisites**, each installed via the same APM convention
   (`git clone` into `~/.vscode/agent-plugins/<publisher>/<repo>`):

---

## Step 1 — Install (APM)

The VS Code **Agent Plugin Manager (APM)** is a directory that GitHub Copilot scans automatically
at startup — there is no `apm` CLI or separate tool to install. The install mechanism is a plain
`git clone` into `~/.vscode/agent-plugins/<publisher>/<repo>`.

This framework and its prerequisites all follow that convention:

```bash
# The SAFe Agentic Organization (the framework application)
git clone https://github.com/poesis-cloud/saf-agentic-organization \
  ~/.vscode/agent-plugins/github.com/poesis-cloud/saf-agentic-organization
```

Reload VS Code. All three orchestrators (`@vmo-orchestrator`, `@rte-orchestrator`,
`@sm-orchestrator`) agents appear in your Copilot Chat `@` list automatically.

**To pin to a specific version:**

```bash
cd ~/.vscode/agent-plugins/github.com/poesis-cloud/saf-agentic-organization
git fetch --tags
git checkout v0.1.0
```

**To update to the latest:**

```bash
cd ~/.vscode/agent-plugins/github.com/poesis-cloud/saf-agentic-organization
git pull
# then reload VS Code: Ctrl+Shift+P → "Developer: Reload Window"
```

> **There is no auto-update.** APM is a directory convention — VS Code reads whatever files are on
> disk at startup. There is no background sync and no notification that a new version is available.
> Updates are manual `git pull`s, applied when you choose.

**Full plugin lifecycle:**

| Operation | Command |
|---|---|
| Install | `git clone <url> ~/.vscode/agent-plugins/<publisher>/<repo>` |
| Update to latest | `cd <apm-path> && git pull` |
| Pin to a version | `cd <apm-path> && git fetch --tags && git checkout vX.Y.Z` |
| Uninstall | `rm -rf ~/.vscode/agent-plugins/<publisher>/<repo>` |

Reload VS Code after any of the above.

---

## Step 2 — Verify agents are visible

1. Restart VS Code (or reload the window: `Ctrl+Shift+P` → "Developer: Reload Window").
2. Open GitHub Copilot Chat.
3. Type `@` — you should see the following agents listed:
   - `@rte-orchestrator` — Release Train Engineer (program/ART layer)
   - `@sm-orchestrator` — Scrum Master (team/iteration layer)
   - `@vmo-orchestrator` — Value Management Office (portfolio layer)

If agents do not appear, see [Troubleshooting](#troubleshooting).

---

## Step 3 — Run your first orchestration

The entry point for new work is `@vmo-orchestrator`. It receives your Epic (the high-level
intent), approves it at ★ Gate 0, and hands it to `@rte-orchestrator` for Feature breakdown.

**Minimal example — start a new Epic:**

Open Copilot Chat and type:

```
@vmo-orchestrator I want to start a new Epic:
"Build a REST API for user authentication (JWT, refresh tokens)"
```

The VMO will:

1. Help you shape the Epic hypothesis and WSJF scoring.
2. Approve it at ★ Gate 0.
3. Dispatch `@rte-orchestrator` to derive Features and plan the sprint.

**Continue to your first PR:**

```
@rte-orchestrator Continue. Derive Features from the Epic and dispatch the SM for Sprint 1.
```

The RTE will derive Features, run architecture triage (★ Gate 2 if needed), and dispatch
`@sm-orchestrator` for Story decomposition and pair programming execution.

---

## Step 4 — Validate success

You have completed the quickstart when:

- [ ] `@vmo-orchestrator`, `@rte-orchestrator`, `@sm-orchestrator` all appear in the agent list.
- [ ] A planning repo structure exists under `portfolio/<slug>/` in your workspace.
- [ ] At least one Story has been executed and a PR has been opened by the SM.

---

## Troubleshooting

**Agents do not appear in the Copilot Chat `@` list**

- Ensure the clone is at the exact path `~/.vscode/agent-plugins/github.com/poesis-cloud/saf-agentic-organization`.
  The `github.com/<org>/<repo>` path structure is required by the VS Code APM convention.
- Reload VS Code window (`Ctrl+Shift+P` → "Developer: Reload Window").
- Check that GitHub Copilot extension is up to date (v1.270 or later recommended).
- Verify `plugins/poesis-saf-agentic-organization/agents/` contains `*.agent.md` files.

**Skills fail to load (agent says "skill not found")**

- Confirm that the orchestration-core skill is present:
  `ls ~/.vscode/agent-plugins/github.com/poesis-cloud/saf-agentic-organization/plugins/poesis-saf-agentic-organization/skills/`

---

## What's next

- Read [CONTRIBUTING.md](https://github.com/poesis-cloud/saf-agentic-organization/blob/main/CONTRIBUTING.md) to understand how to contribute improvements.
- Check [GitHub Releases](https://github.com/poesis-cloud/saf-agentic-organization/releases) for version history.
- File issues at [github.com/poesis-cloud/saf-agentic-organization/issues](https://github.com/poesis-cloud/saf-agentic-organization/issues).
