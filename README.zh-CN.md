# OpenCode Harness Guide 中文版

**语言 / Language：** [简体中文](README.zh-CN.md) | [English](README.md)

先复制 `AGENTS.md`，再填 facts checklist，再选一个 execution contract。只有当前一层已经清楚时，再往后读更高一层。

**[现在开始](#现在开始)** | **[按任务选入口](#按任务选入口)** | **[浏览文件](INDEX.zh-CN.md)** | **[浏览资产](CATALOG.zh-CN.md)**

---

## 现在开始

如果你从零开始，按这个顺序做：

1. 复制 [01-getting-started/templates/AGENTS.md](01-getting-started/templates/AGENTS.md)
2. 用 [02-project-context/templates/PROJECT-FACTS-CHECKLIST.md](02-project-context/templates/PROJECT-FACTS-CHECKLIST.md) 补全事实
3. 从 [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) 里选一个执行合同
4. 如果任务超过一个文件，就从 [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) 开始

只要 repo 不能证明某个命令存在，就继续写成 `TBD`。

说明：当前很多 templates 和 support docs 仍然主要是英文版，中文文档会直接带你跳到这些英文文件，但不会假装它们已经有完整中文版。

---

## 按任务选入口

| 如果你现在要解决…… | 打开这个 | 然后这样做 |
|---|---|---|
| 让 agent 停止猜 | [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md) | 建立或修正 `AGENTS.md` |
| 写清 repo 里的真实事实 | [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md) | 跑 facts checklist |
| 更稳地发任务给 agent | [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md) | 选一个 plan/review/commit/PR 模板 |
| 决定任务该交给谁 | [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md) | 判断 prompt / skill / agent |
| 给系统加内部自动化 | [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md) | 把检查分成 automate/manual |
| 安全接外部系统 | [06-integrations-and-mcp/README.zh-CN.md](06-integrations-and-mcp/README.zh-CN.md) | 写 local integration notes |
| 让团队也能照着用 | [07-team-workflows/README.zh-CN.md](07-team-workflows/README.zh-CN.md) | 跑 onboarding checklist |
| 把 harness 迁移到别的栈 | [08-cross-stack-templates/README.zh-CN.md](08-cross-stack-templates/README.zh-CN.md) | 先分清 universal 和 stack-specific |
| 跑一个更大的编排任务 | [09-advanced-workflows/README.zh-CN.md](09-advanced-workflows/README.zh-CN.md) | 从 kickoff template 开始 |
| 诚实地写命令文档 | [10-cli-and-terminal/README.zh-CN.md](10-cli-and-terminal/README.zh-CN.md) | 逐条验证命令对应真实文件 |
| 理解 plugins / hooks / MCP / OMO | [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md) | 选 built-in / plugin / MCP |
| 用更强的 harness 跑 vibe coding | [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md) | 按 5 步循环执行 |

---

## 用这三种起步模式之一

### 模式 1：repo 有文档，但命令不清楚
- 先看 [01-getting-started/README.zh-CN.md](01-getting-started/README.zh-CN.md)
- 再看 [02-project-context/README.zh-CN.md](02-project-context/README.zh-CN.md)
- 命令一律先保持 `TBD`

### 模式 2：repo 已经有命令，但 agent 输出不稳定
- 先看 [03-commands-and-prompts/README.zh-CN.md](03-commands-and-prompts/README.zh-CN.md)
- 再看 [04-skills-and-agents/README.zh-CN.md](04-skills-and-agents/README.zh-CN.md)
- 先加合同和路由，再谈自动化

### 模式 3：repo 已经有上下文和合同，但工作还是容易混乱
- 先看 [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md)
- 再看 [09-advanced-workflows/README.zh-CN.md](09-advanced-workflows/README.zh-CN.md)
- 需要更强编排时，再看 [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md)

---

## 真实案例

- [examples/nextjs-saas-harness.zh-CN.md](examples/nextjs-saas-harness.zh-CN.md)
- [examples/nextjs-saas-harness.md](examples/nextjs-saas-harness.md)

把这些当成参考结构，不要盲贴。

---

## 当前这个 repo 已验证的事实

- 这是一个 documentation-first 仓库
- 中英文根文档都存在
- `01` 到 `10` 模块都存在
- starter templates 存在
- plugin 和 vibe coding 指南存在
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
