# OpenCode Harness Guide 中文版

**语言 / Language：** [简体中文](README.zh-CN.md) | [English](README.md)

从这里开始。不要先把所有文档看一遍。先把 repo 写清楚，再选一个任务模板，不够用时再往后加。

---

## 现在开始

按这个顺序做：

1. 复制 [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
2. 用 [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) 填事实
3. 选一个任务模板：
   - [03-commands-and-prompts/templates/PLAN-REQUEST.md](03-commands-and-prompts/templates/PLAN-REQUEST.md)
   - [03-commands-and-prompts/templates/REVIEW-REQUEST.md](03-commands-and-prompts/templates/REVIEW-REQUEST.md)
4. 如果任务是多文件或风险更高，就从 [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) 开始

只要 repo 不能证明某个命令存在，就继续写成 `TBD`。

说明：当前很多 templates 和 support docs 仍然主要是英文版，中文文档会直接带你跳到这些英文文件，但不会假装它们已经有完整中文版。

---

## 如果你想直接复制现成的 OpenCode starter pack

从这些文件开始：
- [.opencode/README.zh-CN.md](.opencode/README.zh-CN.md)
- [.opencode/commands/review-docs.md](.opencode/commands/review-docs.md)
- [.opencode/commands/review-readme.md](.opencode/commands/review-readme.md)
- [.opencode/commands/review-module.md](.opencode/commands/review-module.md)
- [.opencode/commands/start-harness-task.md](.opencode/commands/start-harness-task.md)
- [.opencode/agents/docs-review.md](.opencode/agents/docs-review.md)
- [.opencode/agents/doc-link-checker.md](.opencode/agents/doc-link-checker.md)
- [.opencode/agents/harness-planner.md](.opencode/agents/harness-planner.md)
- [.opencode/agents/repo-facts-checker.md](.opencode/agents/repo-facts-checker.md)
- [.opencode/skills/doc-audit/SKILL.md](.opencode/skills/doc-audit/SKILL.md)

复制时保留同样的 `.opencode/` 目录结构。

---

## 按你现在的任务选入口

| 如果你现在要解决…… | 打开这个 | 然后这样做 |
|---|---|---|
| 让 agent 停止猜 | [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md) | 建立或修正 `AGENTS.md` |
| 写清 repo 里的真实事实 | [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md) | 跑 facts checklist |
| 更稳地发任务给 agent | [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) | 选一个任务模板 |
| 创建 command、agent 或 skill | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) | 在 `.opencode/` 里创建对应文件 |
| 给系统加内部自动化 | [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md) | 把检查分成 automate/manual |
| 安全接外部系统 | [06-integrations-and-mcp/README.zh-CN.md](06-integrations-and-mcp/README.zh-CN.md) | 写 local integration notes |
| 让团队也能照着用 | [07-team-workflows/README.zh-CN.md](07-team-workflows/README.zh-CN.md) | 跑 onboarding checklist |
| 把这套做法迁移到别的技术栈 | [08-cross-stack-templates/README.zh-CN.md](08-cross-stack-templates/README.zh-CN.md) | 先分清哪些内容通用，哪些要等真实命令出现再写 |
| 跑一个更大的编排任务 | [09-advanced-workflows/README.zh-CN.md](09-advanced-workflows/README.zh-CN.md) | 从 kickoff template 开始 |
| 诚实地写命令文档 | [10-cli-and-terminal/README.zh-CN.md](10-cli-and-terminal/README.zh-CN.md) | 逐条验证命令对应真实文件 |
| 判断该用 built-in、plugin、MCP 还是 OMO | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) | 先选下一层，再决定要不要复制 starter files |

---


## 如果你想用更强的方式跑 vibe coding

按这个顺序做：
1. 先把 repo facts 写清楚
2. 从 kickoff template 开始
3. 先要求 plan，再允许改文件
4. 必要时把 UI、逻辑、查资料分开给不同 agent
5. 没验证前不要接受输出

把这几个文件一起用：
- [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)
- [examples/nextjs-saas-harness.zh-CN.md](examples/nextjs-saas-harness.zh-CN.md)
- [examples/long-running-app-harness.zh-CN.md](examples/long-running-app-harness.zh-CN.md)
- [.opencode/commands/start-harness-task.md](.opencode/commands/start-harness-task.md)

---

## 如果你只想要一个简单学习顺序

按这个顺序读：
1. [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md)
2. [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md)
3. [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md)
4. [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md)
5. [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md)
6. [06-integrations-and-mcp/README.zh-CN.md](06-integrations-and-mcp/README.zh-CN.md)
7. [07-team-workflows/README.zh-CN.md](07-team-workflows/README.zh-CN.md)
8. [08-cross-stack-templates/README.zh-CN.md](08-cross-stack-templates/README.zh-CN.md)
9. [09-advanced-workflows/README.zh-CN.md](09-advanced-workflows/README.zh-CN.md)
10. [10-cli-and-terminal/README.zh-CN.md](10-cli-and-terminal/README.zh-CN.md)

不需要下一层时，就停下，不要为了“看全”继续往后加复杂度。

---

## 如果你想减少要看的根文档

只看这 2 个：
- 主入口：[README.zh-CN.md](README.zh-CN.md)
- 完整目录：[CATALOG.zh-CN.md](CATALOG.zh-CN.md)

---

## 当前这个 repo 已验证的事实

- 这是一个 documentation-first 仓库
- 中英文入口文档都存在
- `01` 到 `10` 模块都存在
- starter templates 存在
- `.opencode` starter pack 示例已经存在
- 当前没有已验证 package manager
- 当前没有已验证 install / lint / test / typecheck / build 命令

---

## 在贡献或报告敏感问题前先看

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [SECURITY.md](SECURITY.md)
- [SUPPORT.md](SUPPORT.md)
- [LICENSE](LICENSE)
- [.github/SECURITY_REPORTING.md](.github/SECURITY_REPORTING.md)

这个仓库已经公开，但**还没有最终开源许可证**。
