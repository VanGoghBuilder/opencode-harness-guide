# Plugins 与 oh-my-opencode

这份文档解释 **plugins** 在 OpenCode 里的位置、它和 **hooks**、**agents**、**tools**、**MCP servers** 的关系，以及为什么如果你想要更强的编排能力，就值得重点理解 **oh-my-opencode**。

---

## 这份文档是干什么的

如果你在问下面这些问题，就从这里开始：

- OpenCode 说的 **plugin** 到底是什么？
- plugin 和 **MCP server** 有什么区别？
- **hook** 应该放在哪个层次理解？
- 什么情况下只用内建 agent 和 tool 就够了？
- **oh-my-opencode** 是什么？我应该怎么使用它？

---

## 最短版本

可以先用这个能力地图：

| 能力 | 最好理解成什么 | 典型用途 |
|---|---|---|
| **Agents / subagents** | 专门化的推理角色 | 探索、架构、评审、领域任务 |
| **Tools** | 模型可直接调用的具体动作 | 读文件、跑 bash、诊断、编辑、抓取网页 |
| **Plugins** | 扩展 OpenCode 本体的能力层 | 给 OpenCode 加能力、加自动化、加自定义工具 |
| **Hooks** | 插件工作流中的自动化触发点 | 前置检查、后置通知、流程护栏 |
| **MCP servers** | 连接外部系统的标准桥梁 | GitHub、数据库、第三方服务、内部系统 |
| **CLI / TUI** | 用户进入 OpenCode 的终端入口 | 交互式使用、脚本化、终端集成 |

最重要的新手区分是：

- **plugins 是扩展 OpenCode 本身**
- **MCP servers 是把 OpenCode 连接到外部系统**
- **hooks 往往是 plugins 工作流里的一种自动化能力**

---

## 官方术语应该怎么理解

这个仓库优先跟随 OpenCode 官方术语：

- **plugins**：扩展 OpenCode，并可添加自定义工具或自动化行为
- **MCP servers**：通过 Model Context Protocol 暴露外部工具
- **agents**、**commands**、**rules**、**tools**、**skills**：都是独立产品概念

官方文档入口：

- <https://opencode.ai/docs/plugins/>
- <https://opencode.ai/docs/mcp-servers/>
- <https://opencode.ai/docs/tools/>
- <https://opencode.ai/docs/agents/>
- <https://opencode.ai/docs/commands/>
- <https://opencode.ai/docs/rules/>

---

## Plugins、hooks、MCP 分别适合什么

### Plugins

把 plugin 理解成 **OpenCode 的扩展层**。

### Hooks

把 hook 理解成 **自动化触发点**，而不是一个独立大类。

### MCP servers

把 MCP 理解成 **外部系统接入层**。

如果问题本质上是“OpenCode 需要访问本地工具面之外的东西”，那 MCP 通常是更对的抽象。

---

## 什么时候不要先上 plugin 或 MCP

如果你的问题只是：

- 一个本地一次性任务
- 内建工具已经能完成的事
- `explore` 已经足够处理的代码探索
- `oracle` 已经足够处理的判断问题
- `bash` 已经足够处理的命令行任务

那就不要一开始就引入 plugin 或 MCP。

---

## oh-my-opencode 应该怎么定位

最安全的描述方式是：

> **oh-my-opencode 是一个 OpenCode 的社区插件 / 编排层**，它在 OpenCode 之上增加更强的工作流结构、预设代理和额外工具能力。

它**不是** OpenCode 原生内建功能。

公开描述里常见的特征包括：

- background agents
- 预构建的 LSP / AST / MCP 工具
- curated agents
- Claude Code 兼容性

---

## 为什么很多人会用 oh-my-opencode

大家通常是因为它能提供：

- 更强的多代理编排
- 更完整的预设工具能力
- 更明确的规划 / 执行 / 评审工作流
- 比从零开始自己搭流程更快的上手路径

---

## 新手如何使用 oh-my-opencode

对新手来说，最重要的不是记命令，而是先搞清楚边界：

1. 它是**社区扩展**，不是 OpenCode 原生命令集
2. 它适合用在你想要**更多编排和更多预设工作流**的时候
3. 真正复制任何命令或配置前，都应该再去核对它的上游文档

公开材料里常见的使用模式包括：

- 类似 `ultrawork` / `ulw` 这种“直接开始做事”的入口
- 类似 `/start-work` 这种更偏规划和结构化流程的入口

这些都应该被理解为 **oh-my-opencode 的社区工作流模式**，不是 OpenCode 的原生命令。

---

## 命名说明

公开资料里，oh-my-opencode 目前也出现了向 **oh-my-openagent** 过渡的命名迹象。

对新手文档来说，最稳妥的做法是：

- 先写 **oh-my-opencode**
- 同时提醒上游资料中可能也会出现 **oh-my-openagent**
- 不要假设这两个名字未来一定完全稳定不变

---

## 一个实用决策顺序

1. **只用 OpenCode 内建能力**
2. **用 agents + tools**
3. **用 plugins / hooks**
4. **用 MCP**
5. **用 oh-my-opencode**

---

## 接下来读什么

- [05-hooks-and-automation/README.zh-CN.md](05-hooks-and-automation/README.zh-CN.md)
- [06-integrations-and-mcp/README.zh-CN.md](06-integrations-and-mcp/README.zh-CN.md)
- [09-advanced-workflows/README.zh-CN.md](09-advanced-workflows/README.zh-CN.md)
- [10-cli-and-terminal/README.zh-CN.md](10-cli-and-terminal/README.zh-CN.md)

如果你想看英文版，请回到 [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md)。
