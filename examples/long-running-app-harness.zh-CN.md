# Long-Running App Harness 案例

如果任务已经大到不能靠一轮短 session 做完，就用这个案例。

这个案例吸收了 Anthropic 在 long-running application development 里的几个关键做法：
- 规划的人不要和实现的人混在一起
- 实现的人不要自己给自己打高分
- 任务要拆成能单独验收的小块
- 验证要打到真实系统行为，而不是只看代码看起来像完成了

---

## 第 1 步：先分 3 个角色

不要让一个 agent 包打天下。
先分成 3 个角色：

- **Planner**：把短 prompt 扩成可执行计划
- **Builder**：一次只做一个小块
- **Evaluator**：检查这块东西是不是真的能用

在 OpenCode 里，一开始不需要搭很复杂的系统。可以先用：
- `plan` 做规划角色
- `build` 或普通实现流程做 builder
- 单独的 review / QA 流程做 evaluator

如果你想直接复制角色文件，可以从这里开始：
- [../.opencode/agents/harness-planner.md](../.opencode/agents/harness-planner.md)
- [../.opencode/agents/repo-facts-checker.md](../.opencode/agents/repo-facts-checker.md)
- [../.opencode/agents/doc-link-checker.md](../.opencode/agents/doc-link-checker.md)

---

## 第 2 步：先写一个有边界的计划

不要只给一句需求，然后让 builder 连跑几个小时。
先写一个有边界的计划。

直接用：
- [../03-commands-and-prompts/templates/PLAN-REQUEST.md](../03-commands-and-prompts/templates/PLAN-REQUEST.md)
- 或 [../.opencode/commands/start-harness-task.md](../.opencode/commands/start-harness-task.md)

一个好的 long-running 计划至少要写清：
- 这个应用或功能必须做到什么
- 这次大概率会碰哪些文件或区域
- 这轮不做什么
- evaluator 最后拿什么来验收

计划不要写得太死，不然一开始写错，后面全都跟着错。

---

## 第 3 步：把任务拆成小块

不要让 builder 一次做完整个产品。
拆成可以单独验收的小块。

一个常见顺序可以是：
1. app shell 和基础路由
2. 数据模型和存储层
3. 一个核心流程打通
4. auth / permissions
5. 外部集成
6. 打磨和补边界

每一块最后都要回答一个问题：
**evaluator 能不能明确判断这一块是不是完成了？**

如果不能，这一块还是太大、太模糊。

---

## 第 4 步：每一块开工前先写 chunk contract

每一块开始前，先写一个短合同，写清：
- 这块做什么
- 这块不做什么
- evaluator 怎么验

最小例子：

```md
Chunk: user can create and save a project

In scope:
- create project form
- persistence to local database
- project list updates after save

Out of scope:
- sharing projects
- project deletion
- permissions model

The evaluator will check:
- form submits successfully
- saved project appears in the list
- stored data survives a reload
```

这是防止长任务越跑越歪的最简单办法。

---

## 第 5 步：验真实行为，不验“看起来像完成”

这是最关键的一条。
不要因为代码“看起来差不多”就接受结果。

每个 chunk，evaluator 至少要验这些真实行为里的一个或多个：
- 浏览器流程能走通
- API 返回正确结果
- 数据状态真的写进去了
- 需要的文件和路由真的存在
- diagnostics 干净

如果项目有 UI，evaluator 更像 QA tester，不只是 code reviewer。

如果项目有数据状态，就验数据状态，不只验表单长得对不对。

---

## 第 6 步：session 变浑了，就做 handoff

长任务最容易坏在：上下文堆太多、线程太多、builder 越做越乱。
这时不要硬顶着跑。

正确做法：
1. 把当前状态写成短 artifact
2. 把下一块写清楚
3. 只把下一轮必须知道的事实带过去

handoff note 至少包含：
- 已完成什么
- 哪些失败了或需要返工
- 下一块做什么
- 下一轮 evaluator 要验什么

这样就算跨很多 session，harness 也不会散。

---

## 第 7 步：不再必要的 scaffold，就删掉

不要因为某个 scaffold 曾经有用，就永远保留。
如果现在模型已经能稳定处理某一步，就把那层多余 scaffold 拿掉。

规则很简单：
- scaffold 明显提升结果时就加
- scaffold 不再是关键时就删

这样 harness 才会越来越轻，而不是越来越仪式化。

---

## 一套最小可复制的 long-running app 流程

1. 从 [../.opencode/commands/start-harness-task.md](../.opencode/commands/start-harness-task.md) 开始
2. 让 planner 给出分块计划
3. 只批准第一块
4. 让 builder 只做这一块
5. 用 evaluator 去验真实行为
6. 写一个短 handoff note 给下一块
7. 重复直到做完

---

## 这个案例配合这些文件一起用

- [../README.zh-CN.md](../README.zh-CN.md)
- [../09-advanced-workflows/README.zh-CN.md](../09-advanced-workflows/README.zh-CN.md)
- [../03-commands-and-prompts/templates/PLAN-REQUEST.md](../03-commands-and-prompts/templates/PLAN-REQUEST.md)
- [../.opencode/commands/start-harness-task.md](../.opencode/commands/start-harness-task.md)
- [../.opencode/agents/harness-planner.md](../.opencode/agents/harness-planner.md)
