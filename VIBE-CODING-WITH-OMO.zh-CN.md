# Vibe Coding 与 oh-my-opencode 实战

“Vibe coding（意图编程）”是指：主要通过自然语言表达工程意图，把语法细节、文件搜索和具体执行都交给 AI 代理去完成。
但是，没有护栏的 vibe coding 很快就会变成一场灾难：代码改乱、上下文丢失、越改越错。

**oh-my-opencode** 的核心价值，就是为 OpenCode 提供了一套**工程脚手架（Engineering Harness）**。它补足了原生聊天界面缺乏的结构：并行代码探索、明确的规划闸门、专业代理路由以及严格的验证循环。

这是一份手把手教你如何使用 OpenCode + oh-my-opencode 作为日常工作流的操作指南。

---

## 🛠️ 5 步 Vibe Coding 标准工作流

当你安装了 oh-my-opencode 后，不要再像以前那样直接丢一句“帮我改一下按钮颜色”就开始让它写代码。请遵循以下标准循环：

### 第 1 步：建立上下文基座（Context）
在你敲下第一行 prompt 之前，确保你的仓库里有一个基本的 `AGENTS.md`。OpenCode 需要知道你的项目规则，而 oh-my-opencode 派生出的所有子代理都会继承这些规则。
- *你的动作*：确保 `AGENTS.md` 存在且反映当前真实事实。

### 第 2 步：结构化启动（Kickoff）
不要只说“修个 bug”，你要触发一次结构化的工作流。
- *你的动作*：使用结构化的启动模板（参考 [`09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md`](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)）。
- *命令*：根据你使用的社区插件版本，你可以通过 `/start-work`、`ulw`，或者明确要求主控代理“进入分析模式（[analyze-mode]）”来启动。

### 第 3 步：探索与规划闸门（Planning Gate）
主控代理**不会**立刻开始写代码。它会并行派发 `explore` 和 `librarian` 后台代理，去阅读你的代码库或查找外部文档。
- *你的角色*：喝口水，等后台任务完成。
- *把关*：主控代理（或专门的 `plan` 代理）会给出一份计划：要改哪些文件，核心思路是什么。**认真审查这份计划。** 如果设计有缺陷，在写下任何一行代码前纠正它。

### 第 4 步：并行执行（Execution）
计划通过后，主控代理会把任务分发给专业领域的代理（例如把 UI 交给 `visual-engineering`，把硬逻辑交给 `ultrabrain`）。
- *你的角色*：看着任务一个个完成。不要去微观管理语法细节。你现在是 Tech Lead 和 Reviewer，子代理才是打字员。

### 第 5 步：严格验证（Verification）
oh-my-opencode 强调零容忍错误。主控代理会在修改后运行 `lsp_diagnostics`（语言服务器诊断）和编译检查。
- *你的角色*：如果子代理改错了，主控代理会自动打回去重做。只有当诊断工具全绿、测试（如果有的话）通过时，你才算接受这批代码。

---

## 🚫 Vibe Coding 常见反模式（千万别这么做）

如果你在用 oh-my-opencode，请立刻停止这些习惯：

- **盲人摸象式调试（Shotgun Debugging）**：不要贴一段报错然后说“修好它”。你应该说：“*派发 explore 代理去 auth 模块找这个报错的根本原因，然后再向 oracle 代理咨询修复方案。*”
- **微观管理语法**：不要告诉代理正则表达式应该怎么写。告诉代理*你要匹配什么边界情况*，让 `ultrabrain` 自己去搞定语法。
- **跳过规划阶段**：绝对不要允许主控代理在没有向你展示文件清单和意图前，就直接开始修改 5 个文件。
- **跟代理抢活干**：如果主控代理已经派发了后台 agent 去搜代码库，不要在同一个聊天窗口里自己手动去读文件。让系统跑完它的流程。

---

## 🚀 接下来看什么

- 复制启动模板去用：[09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)（目前为英文模板）
- 理解插件和 MCP 的技术边界：[PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md)
