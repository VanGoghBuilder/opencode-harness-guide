# OpenCode Harness Quick Reference

Use this file when you want the shortest path to the next action.

---

## If you only have 15 minutes

Do this in order:
1. Copy [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
2. Fill it using [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md)
3. Pick one execution contract from [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) or [REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md)

Stop there if your repo facts are still unclear.

---

## Open this file when you need...

| Need | File |
|---|---|
| stop the agent from guessing | [01-getting-started/README.md](01-getting-started/README.md) |
| document repo facts | [02-project-context/README.md](02-project-context/README.md) |
| ask for work in a controlled way | [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md) |
| decide prompt vs skill vs agent | [04-skills-and-agents/README.md](04-skills-and-agents/README.md) |
| add internal automation safely | [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md) |
| connect external systems | [06-integrations-and-mcp/README.md](06-integrations-and-mcp/README.md) |
| make the repo usable for teammates | [07-team-workflows/README.md](07-team-workflows/README.md) |
| keep the harness portable | [08-cross-stack-templates/README.md](08-cross-stack-templates/README.md) |
| run a larger orchestrated task | [09-advanced-workflows/README.md](09-advanced-workflows/README.md) |
| verify command docs | [10-cli-and-terminal/README.md](10-cli-and-terminal/README.md) |
| choose built-in vs plugin vs MCP | [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md) |
| run a stronger vibe coding flow | [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md) |

---

## Copy one of these now

- repo entry point: [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
- facts checklist: [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md)
- planning contract: [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md)
- review contract: [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md)
- docs review command pattern: [04-skills-and-agents/README.md](04-skills-and-agents/README.md)
- OMO kickoff: [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)

---

## Keep these boundaries in mind

- if a command is not backed by a real file, keep it as `TBD`
- if a task is local, start with built-in tools and agents
- if a task needs external systems, move to MCP
- if a workflow needs stronger orchestration, study OMO
