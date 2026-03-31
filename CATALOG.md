# OpenCode Catalog

This catalog is the current file index for the `opencode-howto` rewrite.
It lists what is actually present now, what is safe to copy now, and which deeper areas are still planned.

---

## Inventory summary

| Area | Current state |
|------|---------------|
| Root guides | Present |
| Root support docs | Present |
| Numbered modules | Present (`01` through `10`) |
| Starter templates | Present |
| Deeper automation examples | Planned |
| Deeper integration examples | Planned |
| Stack-specific starter kits | Planned |

---

## Root guides and support docs

### Chinese-language entry docs

| File | Purpose |
|------|---------|
| [README.zh-CN.md](README.zh-CN.md) | Chinese root entry point |
| [QUICK_REFERENCE.zh-CN.md](QUICK_REFERENCE.zh-CN.md) | Chinese quick-start path |
| [INDEX.zh-CN.md](INDEX.zh-CN.md) | Chinese browseable root map |
| [LEARNING-ROADMAP.zh-CN.md](LEARNING-ROADMAP.zh-CN.md) | Chinese guided learning path |
| [CATALOG.zh-CN.md](CATALOG.zh-CN.md) | Chinese inventory of docs and starter assets |

### English root guides and support docs

| File | Purpose |
|------|---------|
| [README.md](README.md) | root entry point and current repository overview |
| [QUICK_REFERENCE.md](QUICK_REFERENCE.md) | fastest path for first-time users |
| [INDEX.md](INDEX.md) | browseable root map by need |
| [LEARNING-ROADMAP.md](LEARNING-ROADMAP.md) | recommended learning path |
| [CATALOG.md](CATALOG.md) | current index of files and starter assets |
| [STYLE_GUIDE.md](STYLE_GUIDE.md) | writing and consistency rules for repo docs |
| [CONTRIBUTING.md](CONTRIBUTING.md) | how to improve the repo safely |
| [SECURITY.md](SECURITY.md) | security policy for repository content and templates |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | collaboration expectations for contributors |
| [LICENSE](LICENSE) | current license-status placeholder until a final license is chosen |
| [SUPPORT.md](SUPPORT.md) | support and reporting boundaries for public contributors |
| [CHANGELOG.md](CHANGELOG.md) | documentation milestones for the rewrite |
| [AGENTS.md](AGENTS.md) | repository guidance for coding agents |

### `.github` support files

| File | Purpose |
|------|---------|
| [.github/pull_request_template.md](.github/pull_request_template.md) | pull request structure for repo changes |
| [.github/SECURITY_REPORTING.md](.github/SECURITY_REPORTING.md) | security-reporting guidance for sensitive issues |
| [.github/ISSUE_TEMPLATE/bug_report.md](.github/ISSUE_TEMPLATE/bug_report.md) | public bug intake |
| [.github/ISSUE_TEMPLATE/feature_request.md](.github/ISSUE_TEMPLATE/feature_request.md) | feature request intake |
| [.github/ISSUE_TEMPLATE/documentation.md](.github/ISSUE_TEMPLATE/documentation.md) | documentation issue intake |
| [.github/ISSUE_TEMPLATE/question.md](.github/ISSUE_TEMPLATE/question.md) | question intake |

---

## Numbered modules

| Module | File | Focus |
|--------|------|-------|
| 01 | [01-getting-started/README.md](01-getting-started/README.md) | first session, safe habits, starter `AGENTS.md` |
| 02 | [02-project-context/README.md](02-project-context/README.md) | verified facts, repo context, project guidance |
| 03 | [03-commands-and-prompts/README.md](03-commands-and-prompts/README.md) | reusable planning and review requests, with official command terminology kept separate |
| 04 | [04-skills-and-agents/README.md](04-skills-and-agents/README.md) | when official OpenCode skills or agents help |
| 05 | [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md) | automation boundaries and guardrails |
| 06 | [06-integrations-and-mcp/README.md](06-integrations-and-mcp/README.md) | local integration notes and official MCP-oriented setup guidance |
| 07 | [07-team-workflows/README.md](07-team-workflows/README.md) | onboarding and shared conventions |
| 08 | [08-cross-stack-templates/README.md](08-cross-stack-templates/README.md) | cross-stack planning and universal vs stack-specific guidance |
| 09 | [09-advanced-workflows/README.md](09-advanced-workflows/README.md) | multi-step workflow design and scaling repeated processes |
| 10 | [10-cli-and-terminal/README.md](10-cli-and-terminal/README.md) | TUI/CLI-aware terminal reference guidance |

Chinese translations for the module entry docs now exist as matching `README.zh-CN.md` files in `01` through `10`.

---

## Starter templates available now

| Path | Category | Use |
|------|----------|-----|
| [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md) | project context | minimal starter `AGENTS.md` |
| [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) | project context | facts checklist before writing repo guidance |
| [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) | reusable prompts | starter planning request |
| [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md) | reusable prompts | starter review request |
| [03-commands-and-prompts/templates/COMMIT-REQUEST.md](03-commands-and-prompts/templates/COMMIT-REQUEST.md) | reusable prompts | starter commit message request |
| [03-commands-and-prompts/templates/PR-REQUEST.md](03-commands-and-prompts/templates/PR-REQUEST.md) | reusable prompts | starter pull request generator |
| [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) | skills and agents | decide when specialization is justified |
| [04-skills-and-agents/templates/skills/self-assessment/SKILL.md](04-skills-and-agents/templates/skills/self-assessment/SKILL.md) | skills and agents | starter self-assessment skill template |
| [04-skills-and-agents/templates/skills/self-assessment/README.md](04-skills-and-agents/templates/skills/self-assessment/README.md) | skills and agents | usage notes for the self-assessment starter |
| [05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md) | automation | decide what should and should not be automated |
| [06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) | integrations | document local-only integration setup safely |
| [07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md](07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md) | team workflows | check whether onboarding can happen without guessing |
| [08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md](08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md) | cross-stack planning | check whether a stack-specific starter is actually ready |
| [09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md](09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md) | advanced workflows | decide whether a repeated process is ready to scale |

These files are safe to adapt now as starter docs and checklists, and they work best after reading the matching module. They are intentionally minimal.

---

## What is present vs what is planned

### Present now

- root docs
- root support docs for onboarding, browsing, style, and contribution flow
- repository support docs for security, conduct, and license status
- `.github` support files for PRs, issue intake, and security reporting
- a full first-pass module scaffold from `01` to `10`
- a starter template set across the current learning path

### Still planned

- more templates per module
- executable examples backed by real tooling
- integration configs tied to actual services used by this repo
- stack-specific starter kits with verified commands

---

## What is not safe to assume yet

Until the repository grows real stack-specific files, do not assume:

- a package manager has been chosen
- build, lint, typecheck, test, or single-test commands exist
- any framework-specific starter kit is finalized
- integration configs in this repo are executable and complete

This catalog should keep making that boundary obvious.

---

## Best next additions

The next highest-value additions would be:

1. a richer quickstart with more concrete copy-and-adapt walkthroughs
2. a deeper automation example backed by real repo tooling
3. a deeper integration example backed by real repo tooling
4. the first stack-specific starter kit once verified commands exist

Until then, this repository is correctly optimized for structure, clarity, and honest starter guidance.
