# OpenCode Harness Guide 中文版

**语言 / Language：** [简体中文](README.zh-CN.md) | [English](README.md)

帮助你为 OpenCode 建立一套**工程 harness（工程脚手架 / 控制系统）**：让仓库可被 agent 读取、让约束可被执行、让反馈回路能真正纠错。

**[15 分钟开始](#15-分钟开始)** | **[选择你的 Harness 路径](#选择你的-harness-路径)** | **[查看完整中文索引](INDEX.zh-CN.md)** | **[查看中文目录](CATALOG.zh-CN.md)**

---

## 当前公开状态

这个仓库已经公开，也欢迎贡献，但它**还没有最终开源许可证**。

- 在假设可复用权限前，请先看 [LICENSE](LICENSE)
- 在贡献前，请先看 [CONTRIBUTING.md](CONTRIBUTING.md)
- 在提交敏感问题前，请先看 [SECURITY.md](SECURITY.md) 和 [.github/SECURITY_REPORTING.md](.github/SECURITY_REPORTING.md)

在真正的许可证和私下报告渠道出现之前，请把它理解成一个公开的文档项目，而不是已经完全明确复用边界的开源仓库。

---

## 目录

- [当前公开状态](#当前公开状态)
- [为什么需要这份指南](#为什么需要这份指南)
- [这里说的 Harness 是什么](#这里说的-harness-是什么)
- [Harness 模型](#harness-模型)
- [Plugins 与 oh-my-opencode](#plugins-与-oh-my-opencode)
- [选择你的 Harness 路径](#选择你的-harness-路径)
- [15 分钟开始](#15-分钟开始)
- [Harness 实际使用场景](#harness-实际使用场景)
- [现在已经有什么](#现在已经有什么)
- [现在就能复制的模板](#现在就能复制的模板)
- [常见问题](#常见问题)
- [仓库支持文档](#仓库支持文档)
- [仍在计划中的内容](#仍在计划中的内容)
- [当前仓库现实](#当前仓库现实)

---

## 为什么需要这份指南

很多 AI 编码失败，真正出问题的不是模型本身，而是 **harness 设计失败**。

常见缺口包括：

- 仓库里没有 agent 真正能读懂的 system of record
- 约束条件和边界不清楚
- 执行方式没有固定合同
- 没有反馈回路去验证和纠错
- 长时间之后仓库会进入文档和模式漂移，也就是 entropy

所以，这个仓库现在的目标不只是“教你怎么用 OpenCode”，而是**教你怎么为 OpenCode 设计和维护工程 harness**。

---

## 这里说的 Harness 是什么

这里的 harness，指的是下面这些东西的组合：

- agent 能真正读取的仓库上下文
- 它必须遵守的规则和约束
- 明确表达意图的结构化工作流
- 安全扩展能力的自动化和集成方式
- 能告诉它“改对了没有”的反馈回路
- 能长期控制混乱和漂移的维护机制

好的 harness 不是替人做决策，而是让人负责 steering，让 agent 负责 execution。

---

## Harness 模型

可以先记住这 5 步：

1. **先建地图**：用 `AGENTS.md`、索引和模块文档建立入口
2. **再写事实**：让仓库变成 system of record
3. **再加约束**：用模板、规则、hooks 和边界定义行为
4. **再加反馈回路**：通过诊断、测试、评审和外部信号纠错
5. **再管熵增**：通过文档维护、导航整洁和复查流程维持系统可读性

一句最重要的话：**如果信息不在仓库里，agent 就无法可靠地使用它。**

---

## Plugins 与 oh-my-opencode

如果你最关心的是：**plugins、hooks、MCP 到底怎么区分**，或者你想重点理解 **oh-my-opencode**，请从这里开始：

- [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md)
- [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md)
- [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md)

这个仓库把 **oh-my-opencode** 理解为一个值得学习的**社区 harness 层**，而不是 OpenCode 的原生内建功能。

---

## 选择你的 Harness 路径

| 如果你想…… | 先看 | 然后看 |
|---|---|---|
| 建一个安全的 starter harness | [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md) | [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md) |
| 给 agent 明确意图和执行合同 | [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) |
| 理解 plugins、hooks、MCP 与 oh-my-opencode | [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md) | [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md) |
| 用更强的 harness 跑 Vibe Coding | [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md) | [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) |
| 给系统增加安全自动化与外部能力 | [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md) | [06-integrations-and-mcp/README.zh-CN.md](06-integrations-and-mcp/README.zh-CN.md) |
| 让 harness 能长期支持团队协作 | [07-team-workflows/README.zh-CN.md](07-team-workflows/README.zh-CN.md) | [08-cross-stack-templates/README.zh-CN.md](08-cross-stack-templates/README.zh-CN.md) |

---

## 15 分钟开始

1. 读 [QUICK_REFERENCE.zh-CN.md](QUICK_REFERENCE.zh-CN.md)
2. 复制起步模板 [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
3. 用 [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) 补全真实仓库事实
4. 从 [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) 里选一个执行合同开始使用

这已经足够搭起一个最小 harness：入口、事实、约束，以及一种明确的工作方式。

---

## Harness 实际使用场景

| 使用场景 | 该看什么 |
|---|---|
| 让仓库变成 agent 可读的 system of record | [AGENTS.md](AGENTS.md) + [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md) |
| 防止 agent 发明命令和结构 | [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md) + [PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) |
| 给 agent 更好的执行合同 | [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) + [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md) |
| 引入更强的社区编排层 | [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md) + [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md) |
| 增加外部系统能力但不失控 | [06-integrations-and-mcp/README.zh-CN.md](06-integrations-and-mcp/README.zh-CN.md) + [06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) |
| 减少长期文档和模式漂移 | [07-team-workflows/README.zh-CN.md](07-team-workflows/README.zh-CN.md) + [SUPPORT.md](SUPPORT.md) |

---

## 现在已经有什么

这个仓库已经有一套第一版的 harness 骨架。

### 根文档

- [README.zh-CN.md](README.zh-CN.md)
- [QUICK_REFERENCE.zh-CN.md](QUICK_REFERENCE.zh-CN.md)
- [INDEX.zh-CN.md](INDEX.zh-CN.md)
- [LEARNING-ROADMAP.zh-CN.md](LEARNING-ROADMAP.zh-CN.md)
- [CATALOG.zh-CN.md](CATALOG.zh-CN.md)
- [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md)
- [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md)
- [README.md](README.md)
- [CATALOG.md](CATALOG.md)
- [AGENTS.md](AGENTS.md)

### Harness 模块

| 顺序 | 模块 | Harness 职责 |
|---|---|---|
| 01 | [Getting Started](01-getting-started/README.zh-CN.md) | 建立初始 harness 入口 |
| 02 | [Project Context](02-project-context/README.zh-CN.md) | 把仓库变成 system of record |
| 03 | [Commands and Prompts](03-commands-and-prompts/README.zh-CN.md) | 建立执行合同 |
| 04 | [Skills and Agents](04-skills-and-agents/README.zh-CN.md) | 把任务路由到正确能力 |
| 05 | [Hooks and Automation](05-hooks-and-automation/README.zh-CN.md) | 增加内部扩展和自动化护栏 |
| 06 | [Integrations and MCP](06-integrations-and-mcp/README.zh-CN.md) | 安全接入外部能力 |
| 07 | [Team Workflows](07-team-workflows/README.zh-CN.md) | 让 harness 可以共享和延续 |
| 08 | [Cross-Stack Templates](08-cross-stack-templates/README.zh-CN.md) | 提高可迁移性 |
| 09 | [Advanced Workflows](09-advanced-workflows/README.zh-CN.md) | 编排复杂多阶段工作 |
| 10 | [CLI and Terminal Usage](10-cli-and-terminal/README.zh-CN.md) | 定义终端边界 |

---

## 现在就能复制的模板

| 路径 | Harness 用途 |
|---|---|
| [`01-getting-started/templates/AGENTS.md`](01-getting-started/templates/AGENTS.md) | 最小 harness 入口 |
| [`02-project-context/templates/PROJECT-FACTS-CHECKLIST.md`](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) | agent 可读事实清单 |
| [`03-commands-and-prompts/templates/PLAN-REQUEST.md`](03-commands-and-prompts/templates/PLAN-REQUEST.md) | 规划合同 |
| [`03-commands-and-prompts/templates/REVIEW-REQUEST.md`](03-commands-and-prompts/templates/REVIEW-REQUEST.md) | 评审合同 |
| [`03-commands-and-prompts/templates/COMMIT-REQUEST.md`](03-commands-and-prompts/templates/COMMIT-REQUEST.md) | 变更摘要合同 |
| [`03-commands-and-prompts/templates/PR-REQUEST.md`](03-commands-and-prompts/templates/PR-REQUEST.md) | 合并准备合同 |
| [`04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md`](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) | 能力路由决策辅助 |
| [`05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md`](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md) | 自动化边界检查 |
| [`06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md`](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) | 外部能力记录 |
| [`07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md`](07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md) | 团队共享 onboarding 检查 |
| [`08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md`](08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md) | 跨栈 readiness 检查 |
| [`09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md`](09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md) | 复杂工作流编排检查 |
| [`09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md`](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) | harness 驱动的 Vibe Coding 启动模板 |
| [`examples/nextjs-saas-harness.zh-CN.md`](examples/nextjs-saas-harness.zh-CN.md) | 真实的 Next.js SaaS harness 示例 |

这些都应该被理解为 harness 起步资产，而不是可直接无脑粘贴的成品。

---

## 常见问题

**和以前的 “how-to” 写法相比，最大的变化是什么？**

仓库的中心从“功能教程”转成了“如何为 OpenCode 设计和维护 harness”。

**这里最核心的一条 harness 规则是什么？**

如果信息不在仓库里，agent 就无法可靠地使用它。

**这里能替代 OpenCode 官方文档吗？**

不能。这里是基于官方术语构建的 harness guide 层。

**我应该去哪里验证官方行为？**

先看 <https://opencode.ai/docs/>，重点包括：

- Rules / `AGENTS.md`: <https://opencode.ai/docs/rules/>
- Agents: <https://opencode.ai/docs/agents/>
- Commands: <https://opencode.ai/docs/commands/>
- Tools: <https://opencode.ai/docs/tools/>
- MCP servers: <https://opencode.ai/docs/mcp-servers/>
- Plugins: <https://opencode.ai/docs/plugins/>

---

## 仓库支持文档

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

## 仍在计划中的内容

当前还没有：

- 绑定真实 repo tooling 的更深入 harness walkthrough
- 绑定真实测试或观测系统的 feedback loop 示例
- 有已验证命令的 stack-specific harness kit
- 更深入的 entropy management 与长期维护方法

---

## 当前仓库现实

### 今天已经验证存在

- 仓库仍然是 documentation-first
- 当前没有已验证 package manager
- 当前没有已验证 install / lint / test / typecheck / build 命令
- 中英文根入口都存在
- harness 视角下的 plugin 与 vibe coding 指南已存在

### 这意味着什么

这个仓库已经能教你 **一个好 harness 的形状**，但它还不是一个带可执行工具链的完整参考实现。
