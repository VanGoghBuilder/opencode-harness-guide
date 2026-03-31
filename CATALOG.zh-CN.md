# OpenCode Harness 目录

这是 `opencode-harness-guide` 当前的中文目录。
它说明现在有哪些 harness 资产已经存在、哪些内容可以直接改写使用、以及哪些更深入部分仍属于未来工作。

---

## 概览

| 区域 | 当前状态 |
|---|---|
| 根 Harness 文档 | 已存在 |
| 根支持文档 | 已存在 |
| Harness 模块 | 已存在（`01` 到 `10`） |
| Starter harness 模板 | 已存在 |
| plugin 与 vibe coding 指南 | 已存在 |
| 更深入 feedback loop 示例 | 计划中 |
| stack-specific harness kit | 计划中 |

---

## 根 Harness 文档

| 文件 | 作用 |
|---|---|
| [README.zh-CN.md](README.zh-CN.md) | 中文 Harness 总览 |
| [QUICK_REFERENCE.zh-CN.md](QUICK_REFERENCE.zh-CN.md) | 中文最快路径 |
| [INDEX.zh-CN.md](INDEX.zh-CN.md) | 中文浏览地图 |
| [LEARNING-ROADMAP.zh-CN.md](LEARNING-ROADMAP.zh-CN.md) | 中文构建顺序 |
| [CATALOG.zh-CN.md](CATALOG.zh-CN.md) | 中文资产目录 |
| [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md) | plugin 能力地图 |
| [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md) | Vibe Coding Harness 实战 |
| [README.md](README.md) | 英文 Harness 总览 |
| [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md) | 英文 plugin 能力地图 |
| [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md) | 英文 Vibe Coding Harness 实战 |

### 支持与治理文档

| 文件 | 作用 |
|---|---|
| [STYLE_GUIDE.md](STYLE_GUIDE.md) | 写作与一致性规范 |
| [CONTRIBUTING.md](CONTRIBUTING.md) | 如何安全改进仓库 |
| [SECURITY.md](SECURITY.md) | 安全策略 |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | 协作预期 |
| [SUPPORT.md](SUPPORT.md) | 支持和报告边界 |
| [LICENSE](LICENSE) | 当前许可证状态占位说明 |
| [CHANGELOG.md](CHANGELOG.md) | 文档重写里程碑 |
| [AGENTS.md](AGENTS.md) | coding agents 仓库指南 |

### `.github` 支持文件

| 文件 | 作用 |
|---|---|
| [.github/pull_request_template.md](.github/pull_request_template.md) | PR 结构模板 |
| [.github/SECURITY_REPORTING.md](.github/SECURITY_REPORTING.md) | 安全问题上报指引 |
| [.github/ISSUE_TEMPLATE/bug_report.md](.github/ISSUE_TEMPLATE/bug_report.md) | bug 提交入口 |
| [.github/ISSUE_TEMPLATE/feature_request.md](.github/ISSUE_TEMPLATE/feature_request.md) | 功能请求入口 |
| [.github/ISSUE_TEMPLATE/documentation.md](.github/ISSUE_TEMPLATE/documentation.md) | 文档问题入口 |
| [.github/ISSUE_TEMPLATE/question.md](.github/ISSUE_TEMPLATE/question.md) | 问题入口 |

---

## Harness 模块

| 模块 | 文件 | Harness 职责 |
|---|---|---|
| 01 | [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md) | 建立最初入口 |
| 02 | [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md) | 记录 repo 事实 |
| 03 | [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) | 建立执行合同 |
| 04 | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) | 路由到正确能力 |
| 05 | [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md) | 增加内部护栏 |
| 06 | [06-integrations-and-mcp/README.zh-CN.md](06-integrations-and-mcp/README.zh-CN.md) | 安全增加外部能力 |
| 07 | [07-team-workflows/README.zh-CN.md](07-team-workflows/README.zh-CN.md) | 让 Harness 可长期共享 |
| 08 | [08-cross-stack-templates/README.zh-CN.md](08-cross-stack-templates/README.zh-CN.md) | 提高可迁移性 |
| 09 | [09-advanced-workflows/README.zh-CN.md](09-advanced-workflows/README.zh-CN.md) | 编排复杂工作 |
| 10 | [10-cli-and-terminal/README.zh-CN.md](10-cli-and-terminal/README.zh-CN.md) | 定义执行边界 |

---

## 当前可用 Starter Harness 资产

| 路径 | 类别 | 用途 |
|---|---|---|
| [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md) | harness entry | 最小 harness 入口 |
| [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) | system of record | 事实清单 |
| [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) | execution contracts | planning 合同 |
| [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md) | execution contracts | review 合同 |
| [03-commands-and-prompts/templates/COMMIT-REQUEST.md](03-commands-and-prompts/templates/COMMIT-REQUEST.md) | execution contracts | 变更摘要合同 |
| [03-commands-and-prompts/templates/PR-REQUEST.md](03-commands-and-prompts/templates/PR-REQUEST.md) | execution contracts | 合并准备合同 |
| [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) | capability routing | 路由决策辅助 |
| [04-skills-and-agents/templates/skills/self-assessment/SKILL.md](04-skills-and-agents/templates/skills/self-assessment/SKILL.md) | capability routing | self-assessment skill 模板 |
| [04-skills-and-agents/templates/skills/self-assessment/README.md](04-skills-and-agents/templates/skills/self-assessment/README.md) | capability routing | self-assessment 使用说明 |
| [05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md) | automation | 自动化边界检查 |
| [06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) | integrations | 外部能力记录 |
| [07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md](07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md) | durability | 共享 onboarding 检查 |
| [08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md](08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md) | portability | stack readiness 检查 |
| [09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md](09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md) | orchestration | 重复流程 readiness 检查 |
| [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) | orchestration | harness 驱动的 Vibe Coding 启动模板 |

---

## 当前已有 vs 仍在计划

### 当前已有

- 根 Harness 文档
- 支持与治理文档
- plugin 与 vibe coding harness 指南
- `.github` 支持文件
- 从 `01` 到 `10` 的第一版 Harness 模块结构
- 沿当前学习路径铺开的 starter harness 资产

### 仍在计划

- 绑定真实 tooling 的更深入 feedback loop 示例
- 绑定真实服务的 integration config 示例
- 带已验证命令的 stack-specific harness kit
- 更深入的 entropy management 示例
