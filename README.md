# OpenCode Harness Guide

**Language / 语言：** [English](README.md) | [简体中文](README.zh-CN.md)

Start here. Do not start by reading every file. First make the repo readable, then use one task template, then add more only when needed.

---

## Start now

Do this in order:

1. Copy [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
2. Fill it with [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md)
3. Use one task template:
   - [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md)
   - [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md)
4. If the task is multi-file or risky, start from [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)

If your repo does not prove a command exists, keep it as `TBD`.

---

## If you need a ready-made OpenCode starter pack

Copy from:
- [.opencode/README.md](.opencode/README.md)
- [.opencode/commands/review-docs.md](.opencode/commands/review-docs.md)
- [.opencode/commands/start-harness-task.md](.opencode/commands/start-harness-task.md)
- [.opencode/agents/docs-review.md](.opencode/agents/docs-review.md)
- [.opencode/agents/harness-planner.md](.opencode/agents/harness-planner.md)
- [.opencode/skills/doc-audit/SKILL.md](.opencode/skills/doc-audit/SKILL.md)

Keep the same `.opencode/` folder structure when you copy them.

---

## Pick the next thing you need

| If you need to... | Open this | Then do this |
|---|---|---|
| stop the agent from guessing | [01-getting-started/README.md](01-getting-started/README.md) | create or fix `AGENTS.md` |
| write down repo facts | [02-project-context/README.md](02-project-context/README.md) | run the facts checklist |
| ask for work in a controlled way | [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md) | choose one task template |
| create a command, agent, or skill | [04-skills-and-agents/README.md](04-skills-and-agents/README.md) | create the file in `.opencode/` |
| add internal automation safely | [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md) | classify checks into automate/manual |
| connect an external system | [06-integrations-and-mcp/README.md](06-integrations-and-mcp/README.md) | write local integration notes |
| make the repo usable for teammates | [07-team-workflows/README.md](07-team-workflows/README.md) | run the onboarding checklist |
| reuse the harness in another stack | [08-cross-stack-templates/README.md](08-cross-stack-templates/README.md) | keep stack-specific claims behind real file evidence |
| run a bigger task | [09-advanced-workflows/README.md](09-advanced-workflows/README.md) | start from the kickoff template |
| document commands honestly | [10-cli-and-terminal/README.md](10-cli-and-terminal/README.md) | verify every command against real files |
| decide built-in vs plugin vs MCP vs OMO | [04-skills-and-agents/README.md](04-skills-and-agents/README.md) | choose the next layer and copy starter files only if needed |

---


## If you want a stronger vibe coding workflow

Use this loop:
1. write down repo facts first
2. start from the kickoff template
3. require a plan before edits
4. split UI / logic / external lookup if needed
5. verify before you accept output

Use these files together:
- [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)
- [examples/nextjs-saas-harness.md](examples/nextjs-saas-harness.md)
- [.opencode/commands/start-harness-task.md](.opencode/commands/start-harness-task.md)

---

## If you want one simple learning order

Read in this order:
1. [01-getting-started/README.md](01-getting-started/README.md)
2. [02-project-context/README.md](02-project-context/README.md)
3. [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md)
4. [04-skills-and-agents/README.md](04-skills-and-agents/README.md)
5. [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md)
6. [06-integrations-and-mcp/README.md](06-integrations-and-mcp/README.md)
7. [07-team-workflows/README.md](07-team-workflows/README.md)
8. [08-cross-stack-templates/README.md](08-cross-stack-templates/README.md)
9. [09-advanced-workflows/README.md](09-advanced-workflows/README.md)
10. [10-cli-and-terminal/README.md](10-cli-and-terminal/README.md)

Stop as soon as the next layer is not needed yet.

---

## If you want fewer root docs

Use only these:
- main entry: [README.md](README.md)
- full inventory: [CATALOG.md](CATALOG.md)

---

## Verified repo facts

- this is a documentation-first repo
- English and Chinese entry docs exist
- modules `01` through `10` exist
- starter templates exist
- `.opencode` starter pack examples now exist
- no package manager is currently verified for this repo itself
- no install, lint, test, typecheck, or build commands are currently verified for this repo itself

---

## Before you contribute or report something sensitive

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [SECURITY.md](SECURITY.md)
- [SUPPORT.md](SUPPORT.md)
- [LICENSE](LICENSE)
- [.github/SECURITY_REPORTING.md](.github/SECURITY_REPORTING.md)

This repository is public, but it is **not yet under a final open-source license**.
