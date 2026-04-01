# OpenCode Harness Guide

**Language / 语言：** [English](README.md) | [简体中文](README.zh-CN.md)

Start by copying `AGENTS.md`, filling the facts checklist, and choosing one execution contract. Use the rest of the repo only when the next layer is actually needed.

**[Start now](#start-now)** | **[Pick your next task](#pick-your-next-task)** | **[Browse files](INDEX.md)** | **[Browse assets](CATALOG.md)**

---

## Start now

If you are starting from zero, do this in order:

1. Copy [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
2. Fill in facts with [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md)
3. Use one execution contract from [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md)
4. If the task is larger than one file, use [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)

If your repo does not prove a command exists, keep it as `TBD`.

---

## Pick your next task

| If you need to... | Open this | Then do this |
|---|---|---|
| stop the agent from guessing | [01-getting-started/README.md](01-getting-started/README.md) | create or fix `AGENTS.md` |
| document what is real in the repo | [02-project-context/README.md](02-project-context/README.md) | run the facts checklist |
| ask for work in a controlled way | [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md) | choose a plan/review/commit/PR template |
| route work to the right capability | [04-skills-and-agents/README.md](04-skills-and-agents/README.md) | decide prompt vs skill vs agent |
| add internal automation safely | [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md) | classify checks into automate/manual |
| connect external systems safely | [06-integrations-and-mcp/README.md](06-integrations-and-mcp/README.md) | write local integration notes |
| make the repo usable for teammates | [07-team-workflows/README.md](07-team-workflows/README.md) | run the onboarding checklist |
| keep the harness portable across stacks | [08-cross-stack-templates/README.md](08-cross-stack-templates/README.md) | verify what is universal vs stack-specific |
| run a larger orchestrated task | [09-advanced-workflows/README.md](09-advanced-workflows/README.md) | start from the kickoff template |
| document commands honestly | [10-cli-and-terminal/README.md](10-cli-and-terminal/README.md) | verify every command against real files |
| understand plugins, hooks, MCP, and OMO | [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md) | choose built-in vs plugin vs MCP |
| run vibe coding with a stronger harness | [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md) | follow the 5-step loop |

---

## Use one of these starting patterns

### Pattern 1: Repo has docs but no clear commands
- start with [01-getting-started/README.md](01-getting-started/README.md)
- then [02-project-context/README.md](02-project-context/README.md)
- keep command sections as `TBD`

### Pattern 2: Repo already has commands, but agent output is inconsistent
- start with [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md)
- then [04-skills-and-agents/README.md](04-skills-and-agents/README.md)
- add stronger review and routing rules before adding more automation

### Pattern 3: Repo already has context and contracts, but work still gets chaotic
- start with [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md)
- then [09-advanced-workflows/README.md](09-advanced-workflows/README.md)
- if needed, add a community orchestration layer through [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md)

---

## Real examples

- [examples/nextjs-saas-harness.md](examples/nextjs-saas-harness.md)
- [examples/nextjs-saas-harness.zh-CN.md](examples/nextjs-saas-harness.zh-CN.md)

Use these as reference structures, not as blind copy-paste.

---

## What is verified in this repo right now

- this is a documentation-first repo
- English and Chinese root docs exist
- modules `01` through `10` exist
- starter templates exist
- plugin and vibe-coding guides exist
- no package manager is currently verified
- no install, lint, test, typecheck, or build commands are currently verified for this repo itself

---

## Before you contribute or report something sensitive

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [SECURITY.md](SECURITY.md)
- [SUPPORT.md](SUPPORT.md)
- [LICENSE](LICENSE)
- [.github/SECURITY_REPORTING.md](.github/SECURITY_REPORTING.md)

This repository is public, but it is **not yet under a final open-source license**.
