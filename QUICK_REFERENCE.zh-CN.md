# OpenCode Harness 快速参考

当你只想知道“下一步具体做什么”时，先看这个文件。

---

## 如果你只有 15 分钟

按这个顺序做：
1. 复制 [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
2. 用 [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) 填事实
3. 从 [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md) 或 [REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md) 选一个执行合同

如果 repo facts 还不清楚，就先停在这里，不要往后加复杂度。

---

## 需要这个结果时，打开这个文件

| 需求 | 文件 |
|---|---|
| 让 agent 停止猜 | [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md) |
| 写清 repo facts | [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md) |
| 更稳地发任务 | [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) |
| 判断 prompt / skill / agent | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) |
| 加内部自动化 | [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md) |
| 接外部系统 | [06-integrations-and-mcp/README.zh-CN.md](06-integrations-and-mcp/README.zh-CN.md) |
| 让团队也能照着用 | [07-team-workflows/README.zh-CN.md](07-team-workflows/README.zh-CN.md) |
| 保持跨栈可迁移 | [08-cross-stack-templates/README.zh-CN.md](08-cross-stack-templates/README.zh-CN.md) |
| 跑更大的编排任务 | [09-advanced-workflows/README.zh-CN.md](09-advanced-workflows/README.zh-CN.md) |
| 验证命令文档 | [10-cli-and-terminal/README.zh-CN.md](10-cli-and-terminal/README.zh-CN.md) |
| 选 built-in / plugin / MCP | [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md) |
| 跑更强的 vibe coding 流程 | [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md) |

---

## 现在就复制这些之一

- repo 入口: [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
- facts checklist: [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md)
- planning contract: [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md)
- review contract: [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md)
- docs review command pattern: [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md)
- OMO kickoff: [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)

---

## 记住这几个边界

- repo 不能证明存在的命令，继续写 `TBD`
- 本地任务先用 built-in tools 和 agents
- 需要外部系统时再用 MCP
- 需要更强编排时再研究 OMO
