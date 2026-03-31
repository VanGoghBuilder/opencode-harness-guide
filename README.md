# OpenCode How To

**Language / 语言：** [English](README.md) | [简体中文](README.zh-CN.md)

Go from opening OpenCode for the first time to building repeatable workflows with docs, starter templates, and a clear learning path.

**[Start in 15 minutes](#get-started-in-15-minutes)** | **[Choose your path](#choose-your-path)** | **[Browse the catalog](CATALOG.md)**

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
- [The problem](#the-problem)
- [How this guide helps](#how-this-guide-helps)
- [How it works](#how-it-works)
- [Plugins and oh-my-opencode](#plugins-and-oh-my-opencode)
- [Choose your path](#choose-your-path)
- [Get started in 15 minutes](#get-started-in-15-minutes)
- [Practical use cases](#practical-use-cases)
- [What exists now](#what-exists-now)
- [Starter templates you can copy now](#starter-templates-you-can-copy-now)
- [FAQ](#faq)
- [Repository support docs](#repository-support-docs)
- [What is still planned](#what-is-still-planned)
- [Current repository reality](#current-repository-reality)

---

## The problem

If you are new to OpenCode, the hardest part is usually not a missing feature. It is knowing what to learn first, how to structure a project safely, and how to reuse good patterns without inventing tooling that is not there.

You can often find feature references, but not a clear path. You can find scattered examples, but not a beginner-friendly sequence. And you can find template ideas, but not always enough guidance to know what is safe to copy today.

---

## How this guide helps

`opencode-howto` is a documentation-first rewrite inspired by `claude-howto`, but adapted for OpenCode and checked against the official docs at `https://opencode.ai/docs/` for product terminology.

The project is designed for first-time OpenCode users who want:

- a clear starting point
- a guided learning path
- copyable starter templates
- honest boundaries around what is real now versus planned later

This repository does **not** pretend to have a mature toolchain when it does not. That honesty is part of the design.

---

## How it works

The simplest way to use this repository is as a small progression:

1. **Start safely** with a starter [`AGENTS.md`](01-getting-started/templates/AGENTS.md)
2. **Capture facts** with the [`PROJECT-FACTS-CHECKLIST.md`](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md)
3. **Improve requests** with the planning, review, commit, and PR templates in [`03-commands-and-prompts/`](03-commands-and-prompts/README.md)
4. **Specialize only when needed** with the guidance in [`04-skills-and-agents/`](04-skills-and-agents/README.md)
5. **Scale carefully** into automation, integrations, team workflows, and advanced paths only when the repository is ready

If you want one quick self-check before choosing a path, this repository now also includes a starter self-assessment skill template with usage notes at [`04-skills-and-agents/templates/skills/self-assessment/README.md`](04-skills-and-agents/templates/skills/self-assessment/README.md). It is a template artifact to copy and adapt, not a built-in repo command.

---

## Plugins and oh-my-opencode

If you want the shortest reliable explanation of **plugins vs hooks vs MCP**, or if you specifically want a beginner-friendly explanation of **oh-my-opencode**, start here:

- [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md)
- [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md) (Step-by-step vibe coding harness guide)
- [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md)

That guide is the repository’s main entry point for:

- official plugin terminology
- the difference between OpenCode plugins and MCP servers
- where hooks fit into plugin-driven automation
- why **oh-my-opencode** matters as a community plugin / orchestration layer

---

## Choose your path

Pick the path that best matches what you need right now:

| If you want to... | Start here | Then read |
|---|---|---|
| get a safe beginner starting point | [QUICK_REFERENCE.md](QUICK_REFERENCE.md) | [01-getting-started/README.md](01-getting-started/README.md) |
| write better plan, review, commit, or PR requests | [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md) | [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) |
| understand plugins, hooks, MCP, and oh-my-opencode | [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md) | [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md) |
| use oh-my-opencode for vibe coding (step-by-step guide) | [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md) | [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) |
| decide whether a repeated task deserves a skill or agent | [04-skills-and-agents/README.md](04-skills-and-agents/README.md) | [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) |
| check whether a teammate can start without guessing | [07-team-workflows/README.md](07-team-workflows/README.md) | [07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md](07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md) |

### If you are new to OpenCode

Start here:

1. [QUICK_REFERENCE.md](QUICK_REFERENCE.md)
2. [01-getting-started/README.md](01-getting-started/README.md)
3. [LEARNING-ROADMAP.md](LEARNING-ROADMAP.md)

### If you want to browse by need

Use:

- [INDEX.md](INDEX.md) for a browseable map
- [CATALOG.md](CATALOG.md) for the current file and template inventory

### If you are contributing or operating as an agent

Use:

- [AGENTS.md](AGENTS.md) for repo-grounded agent guidance
- [STYLE_GUIDE.md](STYLE_GUIDE.md) for writing consistency
- [CONTRIBUTING.md](CONTRIBUTING.md) for contribution flow
- [SUPPORT.md](SUPPORT.md) for support and reporting boundaries

---

## Get started in 15 minutes

If you only have a short window, do this:

1. read [QUICK_REFERENCE.md](QUICK_REFERENCE.md)
2. read [01-getting-started/README.md](01-getting-started/README.md)
3. copy [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md), a starter project instruction file
4. replace placeholders using [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md)

That gives you one safe starting doc, one facts checklist, and one obvious next step.

If you want the next layer after that, move to [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md) and copy one reusable request template at a time.

---

## Practical use cases

Here are the most useful things you can do with the repository as it exists today:

| Use case | What to use |
|---|---|
| create a safer starter `AGENTS.md` for a new repo | [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md) + [01-getting-started/README.md](01-getting-started/README.md) |
| verify repository facts before asking OpenCode to change something | [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) |
| reuse a better request for planning or review | [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) + [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md) |
| draft clearer commit and PR text | [03-commands-and-prompts/templates/COMMIT-REQUEST.md](03-commands-and-prompts/templates/COMMIT-REQUEST.md) + [03-commands-and-prompts/templates/PR-REQUEST.md](03-commands-and-prompts/templates/PR-REQUEST.md) |
| learn the plugin capability map and evaluate oh-my-opencode | [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md) |
| start a step-by-step vibe coding session using an engineering harness | [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md) + [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) |
| decide whether a repeated task should stay a prompt or become a reusable skill | [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) |
| test whether a team can onboard without hidden knowledge | [07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md](07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md) |

---

## What exists now

The initial documentation scaffold is present, and the root support docs are starting to fill in.

### Root guides

- [README.md](README.md)
- [QUICK_REFERENCE.md](QUICK_REFERENCE.md)
- [INDEX.md](INDEX.md)
- [LEARNING-ROADMAP.md](LEARNING-ROADMAP.md)
- [CATALOG.md](CATALOG.md)
- [STYLE_GUIDE.md](STYLE_GUIDE.md)
- [CONTRIBUTING.md](CONTRIBUTING.md)
- [SECURITY.md](SECURITY.md)
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)
- [LICENSE](LICENSE) *(license-status placeholder, not an open-source license grant yet)*
- [CHANGELOG.md](CHANGELOG.md)
- [AGENTS.md](AGENTS.md)

### Numbered modules

| Order | Module | Focus |
|------|--------|-------|
| 01 | [Getting started](01-getting-started/README.md) | first session, safe habits, starter `AGENTS.md` |
| 02 | [Project context](02-project-context/README.md) | verified facts, repo guidance, context files |
| 03 | [Commands and prompts](03-commands-and-prompts/README.md) | reusable request structure, with official command terminology kept clearly separate |
| 04 | [Skills and agents](04-skills-and-agents/README.md) | when OpenCode skills or agents help and when a prompt pattern is enough |
| 05 | [Hooks and automation](05-hooks-and-automation/README.md) | automation boundaries, with hooks understood through the official plugins framing |
| 06 | [Integrations and MCP](06-integrations-and-mcp/README.md) | safe integration notes and MCP-oriented guidance aligned with official docs |
| 07 | [Team workflows](07-team-workflows/README.md) | onboarding, shared conventions, repository honesty |
| 08 | [Cross-stack templates](08-cross-stack-templates/README.md) | what stays universal and what should wait for real stack choices |
| 09 | [Advanced workflows](09-advanced-workflows/README.md) | multi-step workflow design, review points, and scaling repeated processes |
| 10 | [CLI and terminal usage](10-cli-and-terminal/README.md) | truthful command documentation and terminal-facing workflow habits |

---

## Starter templates you can copy now

The current starter set is small on purpose.

| Path | Use |
|------|-----|
| [`01-getting-started/templates/AGENTS.md`](01-getting-started/templates/AGENTS.md) | minimal project-context starter |
| [`02-project-context/templates/PROJECT-FACTS-CHECKLIST.md`](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) | checklist for verified facts and `TBD` items |
| [`03-commands-and-prompts/templates/PLAN-REQUEST.md`](03-commands-and-prompts/templates/PLAN-REQUEST.md) | reusable planning request |
| [`03-commands-and-prompts/templates/REVIEW-REQUEST.md`](03-commands-and-prompts/templates/REVIEW-REQUEST.md) | reusable review request |
| [`03-commands-and-prompts/templates/COMMIT-REQUEST.md`](03-commands-and-prompts/templates/COMMIT-REQUEST.md) | starter commit message request |
| [`03-commands-and-prompts/templates/PR-REQUEST.md`](03-commands-and-prompts/templates/PR-REQUEST.md) | starter pull request generator |
| [`04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md`](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) | checklist for deciding when to keep a prompt, create a skill, or use a specialized agent |
| [`04-skills-and-agents/templates/skills/self-assessment/README.md`](04-skills-and-agents/templates/skills/self-assessment/README.md) | starter self-assessment skill template with usage notes |
| [`05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md`](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md) | checklist for deciding what should be automated |
| [`06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md`](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) | safe local integration notes without committed secrets |
| [`07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md`](07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md) | checklist for whether a new contributor can start without guessing |
| [`08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md`](08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md) | checklist for whether a stack-specific starter kit is actually ready |
| [`09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md`](09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md) | checklist for deciding whether a repeated process is ready to scale |
| [`09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md`](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) | starter kickoff template for vibe coding with oh-my-opencode |

These are safe to adapt now as starter docs, and they work best after reading the matching module. They are not full production templates yet.

---

## FAQ

**Why are there no verified commands yet?**

Because this repository is still documentation-first and has not added real package-manager, lint, test, typecheck, or build files yet. Until those files exist, command docs stay `TBD` on purpose.

**What is safe to copy right now?**

The starter templates listed above, especially the project-context, planning, and review templates. They are safe to adapt, but not meant to be pasted blindly without replacing placeholders.

**Is this already an open-source repository in the normal reuse sense?**

Not yet. The repository is public, but [LICENSE](LICENSE) still states that no final open-source license has been chosen. Until that changes, do not assume broad reuse rights.

**Why do some docs emphasize `TBD` and `Not yet present` so much?**

Because the repository is trying to be honest about what is real now. That distinction is one of the core design rules of the rewrite.

**Does this repository replace the official OpenCode documentation?**

No. This repository is a guided learning and starter-template layer. Official product behavior, terminology, and capability boundaries should still be checked against `https://opencode.ai/docs/`.

**Where should I verify official product behavior?**

Start with the official docs index: `https://opencode.ai/docs/`.
For the areas most likely to overlap with this repository, these official pages matter most:

- Rules / `AGENTS.md`: `https://opencode.ai/docs/rules/`
- Agents: `https://opencode.ai/docs/agents/`
- Commands: `https://opencode.ai/docs/commands/`
- Tools: `https://opencode.ai/docs/tools/`
- MCP servers: `https://opencode.ai/docs/mcp-servers/`
- Plugins: `https://opencode.ai/docs/plugins/`
- TUI: `https://opencode.ai/docs/tui/`
- CLI: `https://opencode.ai/docs/cli/`

**Where should contributors start?**

Start with [CONTRIBUTING.md](CONTRIBUTING.md), [STYLE_GUIDE.md](STYLE_GUIDE.md), and [AGENTS.md](AGENTS.md). Then use [INDEX.md](INDEX.md) to find the area you want to improve.

---

## Repository support docs

The repository now also includes basic support and governance docs:

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [SECURITY.md](SECURITY.md)
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)
- [LICENSE](LICENSE)
- [SUPPORT.md](SUPPORT.md)

And under `.github/`:

- [.github/pull_request_template.md](.github/pull_request_template.md)
- [.github/ISSUE_TEMPLATE/bug_report.md](.github/ISSUE_TEMPLATE/bug_report.md)
- [.github/ISSUE_TEMPLATE/feature_request.md](.github/ISSUE_TEMPLATE/feature_request.md)
- [.github/ISSUE_TEMPLATE/documentation.md](.github/ISSUE_TEMPLATE/documentation.md)
- [.github/ISSUE_TEMPLATE/question.md](.github/ISSUE_TEMPLATE/question.md)
- [.github/SECURITY_REPORTING.md](.github/SECURITY_REPORTING.md)

These do not add product features. They make the repository easier to maintain, reuse, and report issues against safely.

---

## What is still planned

The scaffold is present, but deeper material is still planned.

Not yet present:

- stack-specific starter kits with verified commands
- executable examples tied to real package manifests
- deeper automation examples backed by real tooling
- concrete integration configs for actual external systems in this repo
- broader copy-paste assets beyond the current starter set

---

## Current repository reality

### Verified today

- the root docs exist
- the root support docs now include quick reference, index, style guide, contribution guidance, a changelog, and repository support docs for security, conduct, and license status
- modules `01` through `10` exist as README-based documentation
- a starter-template set exists
- no package manager is currently verified in this repository
- no build, lint, typecheck, test, or single-test command is currently verified in this repository
- no Cursor or Copilot rule files are present yet

### What this means for contributors

- prefer documentation and starter templates over speculative code scaffolding
- avoid inventing commands or frameworks
- update files when repo reality changes
- keep future direction separate from present facts

If you follow the root docs plus the numbered modules in order, this repository now has a stronger first-pass learning and support layer. The next phase is deeper examples, richer quickstart material, and eventually real stack-specific starters.
