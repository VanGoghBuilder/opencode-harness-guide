# OpenCode Harness Catalog

This catalog is the current inventory for the `opencode-harness-guide` rewrite.
It explains what harness assets exist now, what is safe to adapt now, and which deeper parts are still future work.

---

## Inventory summary

| Area | Current state |
|------|---------------|
| Root harness docs | Present |
| Root support docs | Present |
| Harness modules | Present (`01` through `10`) |
| Starter harness templates | Present |
| Real-world harness cases | Present |
| Plugin and vibe-coding guides | Present |
| Deeper feedback-loop examples | Planned |
| Stack-specific harness kits | Planned |

---

## Root harness docs

| File | Purpose |
|------|---------|
| [README.md](README.md) | root harness overview |
| [QUICK_REFERENCE.md](QUICK_REFERENCE.md) | fastest harness-building path |
| [INDEX.md](INDEX.md) | browseable harness map by need |
| [LEARNING-ROADMAP.md](LEARNING-ROADMAP.md) | recommended harness build order |
| [CATALOG.md](CATALOG.md) | current inventory of harness assets |
| [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md) | plugin capability map and oh-my-opencode framing |
| [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md) | step-by-step vibe coding harness guide |
| [README.zh-CN.md](README.zh-CN.md) | Chinese root harness overview |
| [QUICK_REFERENCE.zh-CN.md](QUICK_REFERENCE.zh-CN.md) | Chinese fastest harness path |
| [INDEX.zh-CN.md](INDEX.zh-CN.md) | Chinese browseable harness map |
| [LEARNING-ROADMAP.zh-CN.md](LEARNING-ROADMAP.zh-CN.md) | Chinese harness build order |
| [CATALOG.zh-CN.md](CATALOG.zh-CN.md) | Chinese inventory |
| [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md) | Chinese plugin capability map |
| [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md) | Chinese vibe coding harness guide |

### Support and governance docs

| File | Purpose |
|------|---------|
| [STYLE_GUIDE.md](STYLE_GUIDE.md) | writing and consistency rules |
| [CONTRIBUTING.md](CONTRIBUTING.md) | how to improve the repo safely |
| [SECURITY.md](SECURITY.md) | security policy for repository content and templates |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | contributor expectations |
| [SUPPORT.md](SUPPORT.md) | support and reporting boundaries |
| [LICENSE](LICENSE) | current license-status placeholder until a final license is chosen |
| [CHANGELOG.md](CHANGELOG.md) | documentation milestones for the rewrite |
| [AGENTS.md](AGENTS.md) | repository guidance for coding agents |

### `.github` support files

| File | Purpose |
|------|---------|
| [.github/pull_request_template.md](.github/pull_request_template.md) | pull request structure for repo changes |
| [.github/SECURITY_REPORTING.md](.github/SECURITY_REPORTING.md) | security-reporting guidance |
| [.github/ISSUE_TEMPLATE/bug_report.md](.github/ISSUE_TEMPLATE/bug_report.md) | public bug intake |
| [.github/ISSUE_TEMPLATE/feature_request.md](.github/ISSUE_TEMPLATE/feature_request.md) | feature request intake |
| [.github/ISSUE_TEMPLATE/documentation.md](.github/ISSUE_TEMPLATE/documentation.md) | documentation issue intake |
| [.github/ISSUE_TEMPLATE/question.md](.github/ISSUE_TEMPLATE/question.md) | question intake |

---

## Harness modules

| Module | File | Harness job |
|--------|------|-------------|
| 01 | [01-getting-started/README.md](01-getting-started/README.md) | create the initial map |
| 02 | [02-project-context/README.md](02-project-context/README.md) | capture repo facts |
| 03 | [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md) | define execution contracts |
| 04 | [04-skills-and-agents/README.md](04-skills-and-agents/README.md) | route work to the right capability |
| 05 | [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md) | add internal guardrails |
| 06 | [06-integrations-and-mcp/README.md](06-integrations-and-mcp/README.md) | add external capability safely |
| 07 | [07-team-workflows/README.md](07-team-workflows/README.md) | make the harness durable for teams |
| 08 | [08-cross-stack-templates/README.md](08-cross-stack-templates/README.md) | keep the harness portable |
| 09 | [09-advanced-workflows/README.md](09-advanced-workflows/README.md) | orchestrate complex work |
| 10 | [10-cli-and-terminal/README.md](10-cli-and-terminal/README.md) | define execution boundaries |

---

## Starter harness assets available now

| Path | Category | Use |
|------|----------|-----|
| [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md) | harness entry | minimal harness starter |
| [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) | system of record | facts checklist before stronger claims |
| [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) | execution contracts | planning contract |
| [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md) | execution contracts | review contract |
| [03-commands-and-prompts/templates/COMMIT-REQUEST.md](03-commands-and-prompts/templates/COMMIT-REQUEST.md) | execution contracts | change-summary contract |
| [03-commands-and-prompts/templates/PR-REQUEST.md](03-commands-and-prompts/templates/PR-REQUEST.md) | execution contracts | merge-readiness contract |
| [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) | capability routing | specialization decision aid |
| [04-skills-and-agents/templates/skills/self-assessment/SKILL.md](04-skills-and-agents/templates/skills/self-assessment/SKILL.md) | capability routing | starter self-assessment skill template |
| [04-skills-and-agents/templates/skills/self-assessment/README.md](04-skills-and-agents/templates/skills/self-assessment/README.md) | capability routing | usage notes for the self-assessment starter |
| [05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md) | automation | guardrail and automation boundary check |
| [06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) | integrations | document external capability safely |
| [07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md](07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md) | durability | shared onboarding check |
| [08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md](08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md) | portability | stack-readiness check |
| [09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md](09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md) | orchestration | repeated-process readiness check |
| [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) | orchestration | structured kickoff for harness-driven vibe coding |
| [examples/nextjs-saas-harness.md](examples/nextjs-saas-harness.md) | real-world case | Next.js SaaS full harness example |

---

## What is present vs what is planned

### Present now

- root harness docs
- support and governance docs
- plugin and vibe-coding harness guides
- `.github` support files for issue intake and reporting
- a full first-pass harness module scaffold from `01` to `10`
- a starter template set across the current harness path

### Still planned

- deeper feedback-loop examples backed by real tooling
- integration configs tied to actual services used by this repo
- stack-specific harness kits with verified commands
- richer entropy-management examples for long-lived repos

---

## What is not safe to assume yet

Until the repository grows real stack-specific files, do not assume:

- a package manager has been chosen
- build, lint, typecheck, test, or single-test commands exist
- any framework-specific harness kit is finalized
- integration configs in this repo are executable and complete
