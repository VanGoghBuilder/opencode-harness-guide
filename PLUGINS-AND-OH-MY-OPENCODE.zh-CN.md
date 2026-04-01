# Plugins 与 oh-my-opencode

当你需要判断 **下一层该用什么** 时，就看这个文件：built-in tools、plugins、MCP，还是 oh-my-opencode 这种社区 harness layer。

---

## 从这里开始：先选对层

### 如果任务只发生在当前 repo 里
优先用 built-in OpenCode tools：
- 读文件
- 跑 bash
- diagnostics
- 编辑文件
- `explore` / `oracle` 之类内建 agent

### 如果你要扩展 OpenCode 本身
用 plugin：
- 增加内部工作流能力
- 增加 hooks / 自动化行为
- 增加 custom tools

### 如果你要接 repo 外部系统
用 MCP：
- GitHub
- 数据库
- 内部 API
- 第三方系统

### 如果你要一个更强的社区编排层
看 oh-my-opencode：
- 更强的多 agent workflow
- 更完整的 orchestration harness
- 比 raw OpenCode 更“带电”的工作流结构

---

## 5 分钟决策流程

1. 问：**任务是不是只发生在这个 repo 里？**
   - 是 → 先用 built-in tools 和 agents
   - 否 → 进入第 2 步
2. 问：**是不是要访问外部系统？**
   - 是 → 用 MCP
   - 否 → 进入第 3 步
3. 问：**是不是要扩展 OpenCode 自己的内部能力？**
   - 是 → 用 plugin
   - 否 → 保持 built-in 能力即可
4. 问：**我是不是需要比 raw OpenCode 更强的 orchestration？**
   - 是 → 研究 oh-my-opencode
   - 否 → 保持简单

---

## 如果你选了 oh-my-opencode，下一步这样做

1. 把它当成**社区扩展**，不要当成原生 OpenCode 功能
2. 复制任何命令前，先去核对它上游的当前命名
3. 从结构化 kickoff 开始，而不是自由聊天
4. 保留 planning gate：plan 没清楚前不要让它开始改
5. 没有 diagnostics / verification 之前，不要接受输出

如果你要看真正的操作流程，直接打开 [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md)。

---

## 不要这样做

- 不要把 built-in tools 已经能做的事硬塞给 MCP
- 不要因为任务“看起来复杂”就先加 plugin
- 不要把社区插件命令写得像原生 OpenCode commands
- 不要复制上游例子却不核对当前插件行为

---

## 官方文档，用来核对行为

- Plugins: <https://opencode.ai/docs/plugins/>
- MCP servers: <https://opencode.ai/docs/mcp-servers/>
- Tools: <https://opencode.ai/docs/tools/>
- Agents: <https://opencode.ai/docs/agents/>
- Commands: <https://opencode.ai/docs/commands/>
- Rules: <https://opencode.ai/docs/rules/>

---

## 接下来打开这些文件

- [VIBE-CODING-WITH-OMO.zh-CN.md](VIBE-CODING-WITH-OMO.zh-CN.md)
- [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md)
- [06-integrations-and-mcp/README.zh-CN.md](06-integrations-and-mcp/README.zh-CN.md)
- [09-advanced-workflows/README.zh-CN.md](09-advanced-workflows/README.zh-CN.md)
