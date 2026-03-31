# OpenCode Harness 快速参考

如果你想以 **harness builder** 的视角快速浏览仓库，而不是只看功能说明，就用这份文档。

---

## 如果你只有 15 分钟

1. 读 [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md)
2. 复制起步模板 [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
3. 用 [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) 补全真实事实
4. 从 [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) 里选一个执行合同开始用

这已经足够建立一个最小 harness：地图、事实和一份结构化执行方式。

---

## 快速 Harness 路径

按这五步走：

1. **先建地图**
   - [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
   - [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md)
2. **建立执行合同**
   - [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md)
   - [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md)
3. **把任务路由到正确能力**
   - [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md)
   - [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md)
4. **安全扩展能力**
   - [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md)
   - [06-integrations-and-mcp/README.zh-CN.md](06-integrations-and-mcp/README.zh-CN.md)
5. **使用更强的社区编排 harness**
   - [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md)
   - [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md)

---

## 选择你接下来的 15 分钟

| 如果你现在需要…… | 从这里开始 |
|---|---|
| 一个最小可用 harness | [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md) |
| 一个 system of record | [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md) |
| 一份更好的执行合同 | [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) |
| 一份能力路由指南 | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) |
| 一份清楚的 plugin / MCP / hook 解释 | [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md) |
| 一份手把手的 Vibe Coding harness 实战 | [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md) |

---

## 哪个文件回答哪个 Harness 问题

| 问题 | 文件 |
|---|---|
| 这个仓库里的 harness 是什么？ | [README.zh-CN.md](README.zh-CN.md) |
| 我应该先建什么？ | [LEARNING-ROADMAP.zh-CN.md](LEARNING-ROADMAP.zh-CN.md) |
| 当前有哪些文件和模板？ | [CATALOG.zh-CN.md](CATALOG.zh-CN.md) |
| agent 应该遵守什么规则？ | [AGENTS.md](AGENTS.md) |
| 我怎么让仓库变成 agent 可读？ | [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md) |
| 我怎么定义执行合同？ | [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) |
| 我怎么更好地做能力路由？ | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) |
| 我怎么理解 plugins / MCP / hooks？ | [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md) |
| 我怎么跑一套更强的 Vibe Coding 流程？ | [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md) |

---

## 现在就能复制的 Harness 起步模板

| 需求 | 文件 |
|---|---|
| 最小 harness 入口 | [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md) |
| 仓库事实清单 | [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) |
| 规划合同 | [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) |
| 评审合同 | [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md) |
| 能力路由决策检查 | [04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md](04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md) |
| 自动化边界检查 | [05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md](05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md) |
| 本地集成说明 | [06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md) |
| oh-my-opencode Vibe Coding 启动模板 | [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) |

---

## 现在不要假设什么

不要假设：

- 已经选定包管理器
- 已经存在 install / lint / test / typecheck / build 命令
- 已经有完整的 stack-specific harness kit
- 当前 repo 里的集成配置已经能直接执行

只要真实文件还没出现，就继续写 `TBD` 或 `Not yet present`。

---

## 快速路径之后建议读什么

- [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md)
- [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md)
- [INDEX.zh-CN.md](INDEX.zh-CN.md)
- [LEARNING-ROADMAP.zh-CN.md](LEARNING-ROADMAP.zh-CN.md)
