# OpenCode Harness Guide

**Language / 语言：** [English](README.md) | [简体中文](README.zh-CN.md)

Build an **engineering harness** for OpenCode: a repo that agents can read, constraints they can obey, and feedback loops they can use to verify work.

**[Start in 15 minutes](#start-in-15-minutes)** | **[Choose your harness path](#choose-your-harness-path)** | **[Browse the catalog](CATALOG.md)**

---

## Current public status

This repository is public and contribution-ready as a documentation project, but it is **not yet under a final open-source license**.

- Read [LICENSE](LICENSE) before assuming reuse rights.
- Read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a contribution.
- Read [SECURITY.md](SECURITY.md) and [.github/SECURITY_REPORTING.md](.github/SECURITY_REPORTING.md) before reporting anything sensitive.

Until a real license and a real private reporting channel are published, treat this repo as a public project with intentionally limited reuse clarity and no safe private disclosure path hosted inside the repo itself.

---

## Table of contents

- [Current public status](#current-public-status)
- [Why this guide exists](#why-this-guide-exists)
- [What a harness means here](#what-a-harness-means-here)
- [The harness model](#the-harness-model)
- [Plugins and oh-my-opencode](#plugins-and-oh-my-opencode)
- [Choose your harness path](#choose-your-harness-path)
- [Start in 15 minutes](#start-in-15-minutes)
- [Practical harness use cases](#practical-harness-use-cases)
- [What exists now](#what-exists-now)
- [Starter templates you can copy now](#starter-templates-you-can-copy-now)
- [FAQ](#faq)
- [Repository support docs](#repository-support-docs)
- [What is still planned](#what-is-still-planned)
- [Current repository reality](#current-repository-reality)

---

## Why this guide exists

Most AI coding failures are not really model failures. They are **harness failures**.

The agent lacks one or more of these:

- a readable system of record inside the repo
- clear constraints and invariants
- reliable execution boundaries
- fast feedback loops for correction
- maintenance habits that keep the repo from drifting into entropy

This repository is therefore not just a general OpenCode tutorial. It is a guide to building an **OpenCode harness**.

---

## What a harness means here

A harness is the combination of:

- **repo context** the agent can actually read
- **rules and constraints** that limit bad behavior
- **structured prompts and workflows** that make intent explicit
- **automation and integrations** that expand capability safely
- **feedback loops** that tell the agent whether work is actually correct
- **maintenance routines** that keep the system readable over time

A good harness lets humans steer while agents execute.

---

## The harness model

Use this simple progression:

1. **Create the map** with `AGENTS.md`, indexes, and module-level guidance
2. **Capture the facts** so the agent stops guessing
3. **Define constraints** through templates, rules, hooks, and safe boundaries
4. **Add feedback loops** through diagnostics, tests, review, and external signals
5. **Manage entropy** through documentation upkeep, navigation hygiene, and repeatable review habits

If it is not in the repository, the agent cannot reliably use it.

---

## Plugins and oh-my-opencode

If you want the shortest reliable explanation of **plugins vs hooks vs MCP**, or if you specifically want a beginner-friendly explanation of **oh-my-opencode**, start here:

- [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md)
- [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md)
- [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md)

This guide treats **oh-my-opencode** as a community harness layer worth studying, not a built-in OpenCode feature.

---

## Choose your harness path

| If you want to... | Start here | Then read |
|---|---|---|
| build a safe starter harness | [01-getting-started/README.md](01-getting-started/README.md) | [02-project-context/README.md](02-project-context/README.md) |
| define clearer intent and execution contracts | [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md) | [04-skills-and-agents/README.md](04-skills-and-agents/README.md) |
| understand plugins, hooks, MCP, and oh-my-opencode | [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md) | [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md) |
| run vibe coding with a stronger engineering harness | [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md) | [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) |
| add safer automation and external capability | [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md) | [06-integrations-and-mcp/README.md](06-integrations-and-mcp/README.md) |
| make the harness work for teams over time | [07-team-workflows/README.md](07-team-workflows/README.md) | [08-cross-stack-templates/README.md](08-cross-stack-templates/README.md) |

---

## Start in 15 minutes

1. Read [QUICK_REFERENCE.md](QUICK_REFERENCE.md)
2. Copy the starter [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
3. Fill in repo facts using [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md)
4. Pick one structured execution contract from [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md)

That is enough to create a minimal harness: map, facts, constraints, and one explicit way to ask for work.

---

## Practical harness use cases

| Use case | What to use |
|---|---|
| make the repo agent-readable | [AGENTS.md](AGENTS.md) + [02-project-context/README.md](02-project-context/README.md) |
| stop the agent from inventing commands or structure | [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md) + [PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) |
| give the agent a better execution contract | [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) + [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md) |
| add a stronger orchestration layer | [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md) + [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md) |
| add safe external-system capability | [06-integrations-and-mcp/README.md](06-integrations-and-mcp/README.md) + [06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) |
| reduce long-term repo drift | [07-team-workflows/README.md](07-team-workflows/README.md) + [SUPPORT.md](SUPPORT.md) |

---

## What exists now

The repository already has a strong first-pass harness scaffold.

### Root guides

- [README.md](README.md)
- [QUICK_REFERENCE.md](QUICK_REFERENCE.md)
- [INDEX.md](INDEX.md)
- [LEARNING-ROADMAP.md](LEARNING-ROADMAP.md)
- [CATALOG.md](CATALOG.md)
- [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md)
- [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md)
- [STYLE_GUIDE.md](STYLE_GUIDE.md)
- [CONTRIBUTING.md](CONTRIBUTING.md)
- [SECURITY.md](SECURITY.md)
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)
- [LICENSE](LICENSE) *(license-status placeholder, not an open-source license grant yet)*
- [CHANGELOG.md](CHANGELOG.md)
- [AGENTS.md](AGENTS.md)

### Harness modules

| Order | Module | Harness job |
|------|--------|-------------|
| 01 | [Getting started](01-getting-started/README.md) | create the initial harness entry point |
| 02 | [Project context](02-project-context/README.md) | establish the repo as system of record |
| 03 | [Commands and prompts](03-commands-and-prompts/README.md) | define execution contracts |
| 04 | [Skills and agents](04-skills-and-agents/README.md) | route work to the right capability |
| 05 | [Hooks and automation](05-hooks-and-automation/README.md) | add internal extension behavior and guardrails |
| 06 | [Integrations and MCP](06-integrations-and-mcp/README.md) | add external capability safely |
| 07 | [Team workflows](07-team-workflows/README.md) | make the harness shared and durable |
| 08 | [Cross-stack templates](08-cross-stack-templates/README.md) | keep the harness portable across stacks |
| 09 | [Advanced workflows](09-advanced-workflows/README.md) | orchestrate complex multi-step work |
| 10 | [CLI and terminal usage](10-cli-and-terminal/README.md) | define shell and execution boundaries |

---

## Starter templates you can copy now

| Path | Harness use |
|------|-------------|
| [`01-getting-started/templates/AGENTS.md`](01-getting-started/templates/AGENTS.md) | minimal harness entry point |
| [`02-project-context/templates/PROJECT-FACTS-CHECKLIST.md`](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) | facts checklist for agent-readable repos |
| [`03-commands-and-prompts/templates/PLAN-REQUEST.md`](03-commands-and-prompts/templates/PLAN-REQUEST.md) | planning contract |
| [`03-commands-and-prompts/templates/REVIEW-REQUEST.md`](03-commands-and-prompts/templates/REVIEW-REQUEST.md) | review contract |
| [`03-commands-and-prompts/templates/COMMIT-REQUEST.md`](03-commands-and-prompts/templates/COMMIT-REQUEST.md) | change-summary contract |
| [`03-commands-and-prompts/templates/PR-REQUEST.md`](03-commands-and-prompts/templates/PR-REQUEST.md) | merge-readiness contract |
| [`04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md`](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) | capability-routing decision aid |
| [`05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md`](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md) | automation boundary check |
| [`06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md`](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) | external capability notes |
| [`07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md`](07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md) | shared-harness onboarding check |
| [`08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md`](08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md) | portability and readiness check |
| [`09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md`](09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md) | complex-work orchestration check |
| [`09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md`](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) | structured kickoff for harness-driven vibe coding |
| [`examples/nextjs-saas-harness.md`](examples/nextjs-saas-harness.md) | real-world Next.js SaaS harness example |

These are starter harness artifacts, not production-complete drop-ins.

---

## FAQ

**What changed from the older “how-to” framing?**

The center of gravity changed. This repository is now explicitly about **harness engineering for OpenCode**, not just generic feature onboarding.

**What is the main rule of harness engineering here?**

If it is not in the repo, the agent cannot reliably use it.

**Does this repository replace official OpenCode docs?**

No. This repository is a harness-focused guide layer built on top of official OpenCode terminology.

**Where should I verify official product behavior?**

Start with <https://opencode.ai/docs/> and especially:

- Rules / `AGENTS.md`: <https://opencode.ai/docs/rules/>
- Agents: <https://opencode.ai/docs/agents/>
- Commands: <https://opencode.ai/docs/commands/>
- Tools: <https://opencode.ai/docs/tools/>
- MCP servers: <https://opencode.ai/docs/mcp-servers/>
- Plugins: <https://opencode.ai/docs/plugins/>

---

## Repository support docs

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [SECURITY.md](SECURITY.md)
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)
- [SUPPORT.md](SUPPORT.md)
- [LICENSE](LICENSE)
- [.github/pull_request_template.md](.github/pull_request_template.md)
- [.github/ISSUE_TEMPLATE/bug_report.md](.github/ISSUE_TEMPLATE/bug_report.md)
- [.github/ISSUE_TEMPLATE/feature_request.md](.github/ISSUE_TEMPLATE/feature_request.md)
- [.github/ISSUE_TEMPLATE/documentation.md](.github/ISSUE_TEMPLATE/documentation.md)
- [.github/ISSUE_TEMPLATE/question.md](.github/ISSUE_TEMPLATE/question.md)
- [.github/SECURITY_REPORTING.md](.github/SECURITY_REPORTING.md)

---

## What is still planned

Not yet present:

- richer harness walkthroughs tied to real repo tooling
- stronger feedback-loop examples backed by real tests or observability
- stack-specific harness kits once verified commands exist
- deeper entropy-management and long-term maintenance patterns

---

## Current repository reality

### Verified facts today

- the repository is still documentation-first
- no package manager is currently verified
- no install, lint, test, typecheck, or build commands are currently verified
- English and Chinese root entry layers exist
- harness-oriented plugin and vibe-coding guides now exist

### What that means

This repository can already teach the **shape of a good harness**. It is not yet a code-bearing reference implementation with a verified executable toolchain.
