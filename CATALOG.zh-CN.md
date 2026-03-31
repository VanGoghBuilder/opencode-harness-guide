# OpenCode 文档目录（中文版）

**语言 / Language：** [简体中文](CATALOG.zh-CN.md) | [English](CATALOG.md)

这是 `opencode-howto` 当前文件的中文目录。它说明现在真实存在什么、哪些内容适合直接复制、以及哪些更深入的内容还在计划中。

---

## 概览

| 区域 | 当前状态 |
|---|---|
| 英文根文档 | 已存在 |
| 中文根文档 | 已存在 |
| 编号模块 | 已存在（`01` 到 `10`） |
| 中文模块 README | 已存在 |
| 起步模板 | 已存在（当前主要为英文） |
| 更深入的自动化示例 | 计划中 |
| 更深入的集成示例 | 计划中 |
| stack-specific starter kits | 计划中 |

---

## 中文根文档

| 文件 | 作用 |
|---|---|
| [README.zh-CN.md](README.zh-CN.md) | 中文根入口 |
| [QUICK_REFERENCE.zh-CN.md](QUICK_REFERENCE.zh-CN.md) | 中文快速路径 |
| [INDEX.zh-CN.md](INDEX.zh-CN.md) | 中文可浏览索引 |
| [LEARNING-ROADMAP.zh-CN.md](LEARNING-ROADMAP.zh-CN.md) | 中文学习路线图 |
| [CATALOG.zh-CN.md](CATALOG.zh-CN.md) | 中文目录清单 |
| [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md) | plugins 与 oh-my-opencode 指南 |

### 当前仍为英文的支持文档

| 文件 | 作用 |
|---|---|
| [AGENTS.md](AGENTS.md) | 代理行为与仓库事实约束 |
| [STYLE_GUIDE.md](STYLE_GUIDE.md) | 写作与风格规范 |
| [CONTRIBUTING.md](CONTRIBUTING.md) | 贡献流程 |
| [SECURITY.md](SECURITY.md) | 安全策略 |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | 行为规范 |
| [LICENSE](LICENSE) | 许可证状态 |
| [CHANGELOG.md](CHANGELOG.md) | 变更记录 |
| [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md) | 插件能力地图与 oh-my-opencode 指南（英文） |

---

## 中文模块入口

| 模块 | 文件 | 重点 |
|---|---|---|
| 01 | [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md) | 第一次使用、起步习惯、starter `AGENTS.md` |
| 02 | [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md) | 已验证事实、项目上下文、仓库指导 |
| 03 | [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) | 可复用请求结构 |
| 04 | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) | 什么时候该用 skill / agent |
| 05 | [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md) | 自动化边界 |
| 06 | [06-integrations-and-mcp/README.zh-CN.md](06-integrations-and-mcp/README.zh-CN.md) | MCP 与本地集成 |
| 07 | [07-team-workflows/README.zh-CN.md](07-team-workflows/README.zh-CN.md) | onboarding 与共享约定 |
| 08 | [08-cross-stack-templates/README.zh-CN.md](08-cross-stack-templates/README.zh-CN.md) | 通用模式 vs 技术栈细节 |
| 09 | [09-advanced-workflows/README.zh-CN.md](09-advanced-workflows/README.zh-CN.md) | 多阶段工作流 |
| 10 | [10-cli-and-terminal/README.zh-CN.md](10-cli-and-terminal/README.zh-CN.md) | CLI / 终端边界与真实命令文档 |

---

## 当前可用模板（英文原文）

| 路径 | 类别 | 用途 |
|---|---|---|
| [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md) | 项目上下文 | 最小 starter `AGENTS.md` |
| [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) | 项目上下文 | 写仓库说明前先核对事实 |
| [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) | 请求模板 | 计划请求 |
| [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md) | 请求模板 | 评审请求 |
| [03-commands-and-prompts/templates/COMMIT-REQUEST.md](03-commands-and-prompts/templates/COMMIT-REQUEST.md) | 请求模板 | 提交信息请求 |
| [03-commands-and-prompts/templates/PR-REQUEST.md](03-commands-and-prompts/templates/PR-REQUEST.md) | 请求模板 | PR 描述请求 |
| [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) | skills / agents | 判断是否该专业化 |
| [04-skills-and-agents/templates/skills/self-assessment/SKILL.md](04-skills-and-agents/templates/skills/self-assessment/SKILL.md) | skills / agents | self-assessment 模板正文 |
| [04-skills-and-agents/templates/skills/self-assessment/README.md](04-skills-and-agents/templates/skills/self-assessment/README.md) | skills / agents | self-assessment 模板说明 |
| [05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md) | 自动化 | 判断哪些内容该自动化 |
| [06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) | 集成 | 记录本地集成设置 |
| [07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md](07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md) | 团队 | 检查 onboarding 是否清楚 |
| [08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md](08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md) | 技术栈规划 | 检查 stack starter 是否准备好 |
| [09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md](09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md) | 高级流程 | 判断重复流程是否适合扩展 |

---

## 当前已有 vs 仍在计划

### 当前已有

- 中文根入口文档
- 中文模块 README 入口
- 英文模板库
- 英文支持文档
- 完整的 `01` 到 `10` 学习结构

### 仍在计划

- 中文模板正文
- 绑定真实工具链的可执行示例
- 更深入的自动化与集成示例
- 带已验证命令的 stack-specific starter kits
