# OpenCode Quick Reference

Use this file when you want the fastest path through the repository.
It is the shortest root-level guide for first-time OpenCode users.

---

## If you only have 15 minutes

1. Read [01-getting-started/README.md](01-getting-started/README.md)
2. Copy the starter `AGENTS.md` from [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
3. Use [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) to replace placeholders with real repository facts
4. Read [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md) if you want better planning and review requests next

That path is enough to understand the basic workflow and start using one starter template safely.

---

## Fast copy-and-adapt path

Use this repo in five moves:

1. **Start with context**
   - [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
   - [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md)
2. **Improve your requests**
   - [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md)
   - [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md)
   - [03-commands-and-prompts/templates/COMMIT-REQUEST.md](03-commands-and-prompts/templates/COMMIT-REQUEST.md)
   - [03-commands-and-prompts/templates/PR-REQUEST.md](03-commands-and-prompts/templates/PR-REQUEST.md)
3. **Decide whether to specialize**
   - [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md)
   - [04-skills-and-agents/templates/skills/self-assessment/README.md](04-skills-and-agents/templates/skills/self-assessment/README.md)
4. **Add guardrails only when justified**
   - [05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md)
   - [06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md)
5. **Understand extensions and orchestration**
   - [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md)

---

## Choose your next 15 minutes

| If you need... | Start here |
|---|---|
| a safe starting doc for a new project | [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md) |
| a way to document what is real in the repo | [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) |
| a better plan or review request | [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md) |
| a clear plugin vs MCP vs hook explanation | [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md) |
| help deciding whether specialization is worth it | [04-skills-and-agents/README.md](04-skills-and-agents/README.md) |
| a quick team-readiness check | [07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md](07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md) |

---

## Which file answers which question

| Question | File |
|----------|------|
| What is this repo for? | [README.md](README.md) |
| What should I learn first? | [LEARNING-ROADMAP.md](LEARNING-ROADMAP.md) |
| What files and templates exist now? | [CATALOG.md](CATALOG.md) |
| What rules should coding agents follow here? | [AGENTS.md](AGENTS.md) |
| How do I start without inventing commands? | [01-getting-started/README.md](01-getting-started/README.md) |
| How do I document repository facts honestly? | [02-project-context/README.md](02-project-context/README.md) |
| How do I ask for a better plan or review? | [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md) |
| How do I know whether specialization is worth it? | [04-skills-and-agents/README.md](04-skills-and-agents/README.md) |
| How do I check team readiness? | [07-team-workflows/README.md](07-team-workflows/README.md) |

---

## Safe starter templates to copy now

| Need | File |
|------|------|
| Minimal project guidance | [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md) |
| Repo-facts checklist | [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) |
| Planning request | [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) |
| Review request | [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md) |
| Commit message request | [03-commands-and-prompts/templates/COMMIT-REQUEST.md](03-commands-and-prompts/templates/COMMIT-REQUEST.md) |
| Pull request draft | [03-commands-and-prompts/templates/PR-REQUEST.md](03-commands-and-prompts/templates/PR-REQUEST.md) |
| Specialization decision check | [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) |
| Self-assessment skill template | [04-skills-and-agents/templates/skills/self-assessment/README.md](04-skills-and-agents/templates/skills/self-assessment/README.md) |
| Automation boundary check | [05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md) |
| Local integration notes | [06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) |

These files are safe to adapt now. They are starter docs, not production-ready drop-ins.

---

## What not to assume yet

Do not assume:

- a package manager is chosen
- install, lint, test, typecheck, or build commands exist
- any stack-specific starter kit is complete
- integration configs in this repo are executable

Use `TBD` and `Not yet present` until real files support stronger claims.

---

## Best next reads after the fast path

- [04-skills-and-agents/README.md](04-skills-and-agents/README.md)
- [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md)
- [INDEX.md](INDEX.md) for a browseable root map
- [STYLE_GUIDE.md](STYLE_GUIDE.md) if you are writing or editing repo docs

If you want the guided full path instead of the fast path, go to [LEARNING-ROADMAP.md](LEARNING-ROADMAP.md).
