# OpenCode How To 中文版

**语言 / Language：** [简体中文](README.zh-CN.md) | [English](README.md)

帮助你从第一次打开 OpenCode，逐步走到能建立可复用工作流：用文档、起步模板和清晰学习路径，把常见做法固定下来。

**[15 分钟开始](#15-分钟开始)** | **[选择你的路径](#选择你的路径)** | **[查看完整中文索引](INDEX.zh-CN.md)**

---

## 目录

- [问题是什么](#问题是什么)
- [这份指南怎么帮你](#这份指南怎么帮你)
- [它是怎么工作的](#它是怎么工作的)
- [选择你的路径](#选择你的路径)
- [15 分钟开始](#15-分钟开始)
- [当前能解决的实际问题](#当前能解决的实际问题)
- [现在仓库里已经有什么](#现在仓库里已经有什么)
- [现在就能复制使用的模板](#现在就能复制使用的模板)
- [常见问题](#常见问题)
- [仓库支持文档](#仓库支持文档)
- [仍在计划中的内容](#仍在计划中的内容)
- [当前仓库现实](#当前仓库现实)

---

## 问题是什么

如果你刚开始用 OpenCode，最难的通常不是少了某个功能，而是不知道应该先学什么、怎么安全地组织项目上下文、以及哪些做法现在就能复制，哪些还只是未来方向。

你也许能找到零散功能介绍，但找不到一条适合新手的路径；你也许能找到一些例子，但不确定哪些在当前仓库里已经真实存在、哪些只是想法。

---

## 这份指南怎么帮你

`opencode-howto` 是一个文档优先的重写仓库。它受 `claude-howto` 启发，但内容针对 OpenCode 调整，并尽量与官方文档 `https://opencode.ai/docs/` 的术语保持一致。

这个仓库面向的是第一次使用 OpenCode 的人，重点提供：

- 清楚的起点
- 渐进式学习路径
- 可以直接复制和改写的起步模板
- 对“当前真实存在”和“未来计划内容”的明确边界

它不会假装自己已经有成熟的工具链。对当前现实诚实，本身就是设计目标的一部分。

---

## 它是怎么工作的

最简单的使用方式，是把这个仓库当成一条小而清晰的路径：

1. 先用起步版 [`AGENTS.md`](01-getting-started/templates/AGENTS.md) 把 OpenCode 锚定在现实上
2. 用 [`PROJECT-FACTS-CHECKLIST.md`](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) 记录已验证事实
3. 用 [`03-commands-and-prompts/README.zh-CN.md`](03-commands-and-prompts/README.zh-CN.md) 里的请求模板改进计划、评审、提交和 PR 描述
4. 再决定什么时候需要技能或代理，而不是一开始就过度复杂化
5. 最后在仓库成熟后，再进入自动化、集成、团队协作和高级工作流

如果你想先做一个自检，仓库里现在也有一个 self-assessment 技能模板说明页：[`04-skills-and-agents/templates/skills/self-assessment/README.md`](04-skills-and-agents/templates/skills/self-assessment/README.md)。它是一个模板资产，不是仓库里已经启用的内建命令。

---

## 选择你的路径

按你当前最想解决的问题开始：

| 如果你想要…… | 先看 | 然后看 |
|---|---|---|
| 一个安全的新手起点 | [QUICK_REFERENCE.zh-CN.md](QUICK_REFERENCE.zh-CN.md) | [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md) |
| 更好的计划 / 评审 / 提交 / PR 请求写法 | [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) | [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) 等英文模板文件 |
| 判断重复任务是否值得做成技能或代理 | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) | [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) |
| 检查团队是否能无猜测上手 | [07-team-workflows/README.zh-CN.md](07-team-workflows/README.zh-CN.md) | [07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md](07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md) |

### 如果你是第一次使用 OpenCode

建议按这个顺序：

1. [QUICK_REFERENCE.zh-CN.md](QUICK_REFERENCE.zh-CN.md)
2. [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md)
3. [LEARNING-ROADMAP.zh-CN.md](LEARNING-ROADMAP.zh-CN.md)

### 如果你想按需求浏览

- 用 [INDEX.zh-CN.md](INDEX.zh-CN.md) 浏览完整中文索引
- 用 [CATALOG.zh-CN.md](CATALOG.zh-CN.md) 查看当前文件和模板清单

### 如果你需要贡献规则或代理规则

这部分目前仍以英文为主：

- [AGENTS.md](AGENTS.md)
- [STYLE_GUIDE.md](STYLE_GUIDE.md)
- [CONTRIBUTING.md](CONTRIBUTING.md)

---

## 15 分钟开始

如果你现在只有很短的时间，按这个顺序做：

1. 读 [QUICK_REFERENCE.zh-CN.md](QUICK_REFERENCE.zh-CN.md)
2. 读 [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md)
3. 参考英文模板 [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
4. 用 [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) 把占位内容替换成真实仓库事实

这样你会得到一个安全起步文档、一个事实核对清单，以及一个明确的下一步。

如果你想继续往下走，下一层就是 [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md)。

---

## 当前能解决的实际问题

| 使用场景 | 该看什么 |
|---|---|
| 给新仓库写一个更可靠的 `AGENTS.md` 起步版 | [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md) + [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md) |
| 在让 OpenCode 改东西前先确认仓库事实 | [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md) + [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) |
| 复用更好的计划或评审请求 | [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) |
| 写更清楚的 commit / PR 描述 | [03-commands-and-prompts/templates/COMMIT-REQUEST.md](03-commands-and-prompts/templates/COMMIT-REQUEST.md) + [03-commands-and-prompts/templates/PR-REQUEST.md](03-commands-and-prompts/templates/PR-REQUEST.md) |
| 判断一个重复任务是否值得做成 skill / agent | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) |
| 检查团队是否能无隐藏知识地开始使用 | [07-team-workflows/README.zh-CN.md](07-team-workflows/README.zh-CN.md) |

---

## 现在仓库里已经有什么

当前已经有：

- 英文根文档入口层
- 中文根文档入口层（本次新增）
- `01` 到 `10` 的模块 README 中英双入口
- 一组可复制的起步模板（模板正文当前仍是英文）
- 根层支持文档，如贡献、风格、安全、行为规范等

### 当前中文根文档

- [README.zh-CN.md](README.zh-CN.md)
- [QUICK_REFERENCE.zh-CN.md](QUICK_REFERENCE.zh-CN.md)
- [INDEX.zh-CN.md](INDEX.zh-CN.md)
- [LEARNING-ROADMAP.zh-CN.md](LEARNING-ROADMAP.zh-CN.md)
- [CATALOG.zh-CN.md](CATALOG.zh-CN.md)

### 当前中文模块入口

`01-getting-started/README.zh-CN.md` 到 `10-cli-and-terminal/README.zh-CN.md`

---

## 现在就能复制使用的模板

下面这些模板文件当前都是真实存在的，但**模板正文仍为英文版**：

| 路径 | 用途 |
|---|---|
| [`01-getting-started/templates/AGENTS.md`](01-getting-started/templates/AGENTS.md) | 最小可用的项目上下文起步文件 |
| [`02-project-context/templates/PROJECT-FACTS-CHECKLIST.md`](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) | 事实核对清单 |
| [`03-commands-and-prompts/templates/PLAN-REQUEST.md`](03-commands-and-prompts/templates/PLAN-REQUEST.md) | 计划请求模板 |
| [`03-commands-and-prompts/templates/REVIEW-REQUEST.md`](03-commands-and-prompts/templates/REVIEW-REQUEST.md) | 评审请求模板 |
| [`03-commands-and-prompts/templates/COMMIT-REQUEST.md`](03-commands-and-prompts/templates/COMMIT-REQUEST.md) | 提交信息请求模板 |
| [`03-commands-and-prompts/templates/PR-REQUEST.md`](03-commands-and-prompts/templates/PR-REQUEST.md) | PR 描述请求模板 |
| [`04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md`](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) | 判断是否需要技能/代理 |
| [`04-skills-and-agents/templates/skills/self-assessment/SKILL.md`](04-skills-and-agents/templates/skills/self-assessment/SKILL.md) | self-assessment 技能模板正文 |
| [`05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md`](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md) | 自动化边界检查 |
| [`06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md`](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) | 本地集成说明 |
| [`07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md`](07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md) | 团队 onboarding 检查 |
| [`08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md`](08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md) | 技术栈 starter readiness |
| [`09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md`](09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md) | 高级工作流检查清单 |

---

## 常见问题

**为什么这里没有已验证的安装、测试或构建命令？**

因为这个仓库目前仍然是文档优先阶段，还没有真实的包管理器、测试框架或构建链文件。只要这些文件不存在，相关命令就应该保持 `TBD`。

**中文版是不是把所有内容都翻译完了？**

这次范围是：根层入口文档 + `01` 到 `10` 的模块 README。模板正文和部分支持文档目前仍为英文。

**我现在最适合复制什么？**

最适合复制的是起步模板和请求模板，但复制之后要立刻替换占位信息，不要盲贴。

**这里能替代官方 OpenCode 文档吗？**

不能。这里更像学习路径和起步模板层；涉及产品真实行为、术语和边界时，仍然应当回到 `https://opencode.ai/docs/`。

---

## 仓库支持文档

当前这些支持文档仍以英文为主：

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [SECURITY.md](SECURITY.md)
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)
- [LICENSE](LICENSE)
- [AGENTS.md](AGENTS.md)
- [STYLE_GUIDE.md](STYLE_GUIDE.md)

它们不增加产品功能，但会影响仓库维护、协作方式和代理行为。

---

## 仍在计划中的内容

当前还没有：

- 带已验证命令的 stack-specific starter kits
- 绑定真实 package manifest 的可执行例子
- 更深入的自动化和集成示例
- 中文版模板正文和更多中文支持文档

---

## 当前仓库现实

### 今天已经验证存在

- 英文根文档存在
- 中文根文档入口存在
- `01` 到 `10` 的模块中英 README 入口存在
- 一组英文起步模板存在
- 当前没有已验证的 package manager / build / lint / test / typecheck 命令

### 这意味着什么

- 优先使用文档和模板，不要假设代码脚手架已经准备好
- 不要发明不存在的命令
- 模板可以复制，但要按真实仓库情况改写
- 当前的中文层已经能支撑完整阅读路径，但模板正文仍主要是英文
