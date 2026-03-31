# OpenCode 快速参考（中文版）

**语言 / Language：** [简体中文](QUICK_REFERENCE.zh-CN.md) | [English](QUICK_REFERENCE.md)

当你只想快速知道“现在该看哪一个文件”时，用这份文档。

---

## 如果你只有 15 分钟

1. 读 [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md)
2. 参考起步模板 [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
3. 用 [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) 替换占位内容，记录真实仓库事实
4. 如果你还想把请求写得更稳一点，再读 [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md)

---

## 快速复制与改写路径

按这五步走：

1. **先建立上下文**
   - [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
   - [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md)
2. **再改进请求写法**
   - [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md)
   - [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md)
   - [03-commands-and-prompts/templates/COMMIT-REQUEST.md](03-commands-and-prompts/templates/COMMIT-REQUEST.md)
   - [03-commands-and-prompts/templates/PR-REQUEST.md](03-commands-and-prompts/templates/PR-REQUEST.md)
3. **判断是否需要专业化**
   - [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md)
   - [04-skills-and-agents/templates/skills/self-assessment/README.md](04-skills-and-agents/templates/skills/self-assessment/README.md)
4. **最后再加边界与集成**
   - [05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md)
   - [06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md)
5. **理解扩展与编排能力**
   - [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md)

> 这些模板文件当前仍为英文原文，但中文模块会解释它们应该怎么用。

---

## 选择你接下来的 15 分钟

| 如果你现在需要…… | 从这里开始 |
|---|---|
| 新项目的安全起步文档 | [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md) |
| 记录仓库真实状态的方法 | [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md) |
| 更好的计划或评审请求 | [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) |
| 一份清楚的 plugin / MCP / hook 解释 | [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md) |
| 一份手把手的 Vibe Coding 实战工作流指南 | [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md) |
| 判断什么时候该用技能或代理 | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) |
| 检查团队 onboarding 是否清晰 | [07-team-workflows/README.zh-CN.md](07-team-workflows/README.zh-CN.md) |

---

## 哪个问题该看哪个文件

| 问题 | 文件 |
|---|---|
| 这个仓库是干什么的？ | [README.zh-CN.md](README.zh-CN.md) |
| 我应该先学什么？ | [LEARNING-ROADMAP.zh-CN.md](LEARNING-ROADMAP.zh-CN.md) |
| 当前有哪些文档和模板？ | [CATALOG.zh-CN.md](CATALOG.zh-CN.md) |
| 我怎么开始而不发明命令？ | [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md) |
| 我怎么诚实记录仓库事实？ | [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md) |
| 我怎么写更好的计划或评审请求？ | [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) |
| 我怎么判断专业化值不值得？ | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) |
| 我怎么检查团队 readiness？ | [07-team-workflows/README.zh-CN.md](07-team-workflows/README.zh-CN.md) |

---

## 现在就能复制的起步模板

| 需求 | 文件 |
|---|---|
| 最小项目说明 | [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md) |
| 仓库事实核对 | [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) |
| 计划请求 | [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) |
| 评审请求 | [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md) |
| 提交信息请求 | [03-commands-and-prompts/templates/COMMIT-REQUEST.md](03-commands-and-prompts/templates/COMMIT-REQUEST.md) |
| PR 描述请求 | [03-commands-and-prompts/templates/PR-REQUEST.md](03-commands-and-prompts/templates/PR-REQUEST.md) |
| 专业化决策检查 | [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) |
| self-assessment 技能模板说明 | [04-skills-and-agents/templates/skills/self-assessment/README.md](04-skills-and-agents/templates/skills/self-assessment/README.md) |
| 自动化边界检查 | [05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md) |
| 本地集成说明 | [06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) |

这些模板目前都是真实存在的，但正文以英文为主。复制之后请结合你的仓库现实改写。

---

## 现在不要假设什么

不要假设：

- 已经选定了包管理器
- 已经有 install / lint / test / build 命令
- 已经有完整的 stack-specific starter kit
- 这里的集成配置已经是可直接执行的成品

只要真实文件还没出现，就继续写 `TBD` 或 `Not yet present`。

---

## 快速路径之后建议读什么

- [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md)
- [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md)
- [INDEX.zh-CN.md](INDEX.zh-CN.md)
- [CATALOG.zh-CN.md](CATALOG.zh-CN.md)

如果你想走完整路径，而不是只找快速入口，请看 [LEARNING-ROADMAP.zh-CN.md](LEARNING-ROADMAP.zh-CN.md)。
