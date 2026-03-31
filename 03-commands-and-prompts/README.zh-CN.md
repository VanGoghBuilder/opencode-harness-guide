# Commands and Prompts

> **Harness 职责**：这个模块为 agent 提供明确执行合同，而不是模糊聊天意图。

这个模块讨论可复用的请求结构，以及如何把“自然语言意图”变成可以稳定执行的合同。

---

## 为什么这很重要

再强的 agent，如果收到的是模糊请求，也会失败。
问题往往不在模型，而在于请求没有给出：范围、目标、停止条件和输出形状。

这个模块就是用来把“聊天”升级成“执行合同”的。

---

## 🧭 这个模块适合谁

如果你经常遇到这些问题，就看这一章：
- 每次都从头写一大段指令
- 规划、评审、提交说明的质量不稳定
- 分不清 built-in commands 和 repo-specific/community workflow

---

## ⏱️ 15 分钟内你能完成什么

读完之后，你应该能：
1. 区分 built-in commands 和 prompt contracts
2. 把一个模糊请求重写成结构化执行合同
3. 为 planning / review / commit / PR 选择合适模板

---

## 这个模块假设什么，不假设什么

这个模块假设：
- 你已经有一些 repo context
- 你想通过措辞控制 agent 的行为

这个模块不假设：
- 你的 repo 有自定义 slash commands
- repo 已经有 automation 或 plugin 支持
- 每个工作流都已经有可执行 tooling 支撑

---

## 🧠 Commands 和 execution contract 的区别

在 OpenCode 里：
- **Commands** 是 built-in 能力，例如 `/skills`、`/playwright` 等，或者系统原生工具
- **Prompt contracts** 是你写给 agent 的结构化请求，用来规定它该做什么、不该做什么、结果应该长什么样

从 harness 角度看：
- commands 提供 capability
- contracts 约束 execution

---

## Demo case：把一个模糊文档任务改写成执行合同

### 弱请求
“帮我 review 一下这个项目并改进文档。”

### 为什么它会失败
agent 仍然要自己猜：
- review 哪些文档？
- 是只分析还是直接改？
- 优先改结构、措辞还是导航？
- 结果要以什么格式给你？

### 更强的 harness contract
一个好的结构应该至少写清：
- 先 gather context
- 目标是什么
- 有哪些 file hints
- 哪些假设不能做
- 结果如何输出
- 什么时候必须停下来等批准

这正是这个模块里这些模板的用途。

---

## 🛠️ Step-by-step workflow

1. **先判断任务类型**
   - planning
   - review
   - commit summary
   - PR summary
2. **选对应模板**
3. **补全真实上下文**
   - repo area
   - goal
   - constraints
   - output shape
4. **在发送前消除歧义**
   - 要不要先分析？
   - 要不要先出 plan？
   - 要不要等待批准？
5. **写明停止条件**
6. **根据结果反向优化合同，而不只是继续追问**

---

## 对比示例

### 模糊版本
“能帮我写个 PR 吗？”

### 合同版本
“请分析当前分支和最近提交，生成一份 PR 描述，包含 Summary、Motivation、Changes made、How to test、Impact。不要发明命令或 issue 编号。”

第二种写法更像 harness contract，而不是普通聊天。

---

## 常见失败模式与修复

### 失败模式 1：混淆 built-in commands 和社区工作流
修复：把 built-in 和 community / repo-specific workflow 分开写。

### 失败模式 2：一个 prompt 里塞太多不相关任务
修复：一个合同只做一个主输出。

### 失败模式 3：真正需要先分析，却直接要求实现
修复：在合同里加 planning gate。

---

## Starter assets

使用：
- [`templates/PLAN-REQUEST.md`](templates/PLAN-REQUEST.md)
- [`templates/REVIEW-REQUEST.md`](templates/REVIEW-REQUEST.md)
- [`templates/COMMIT-REQUEST.md`](templates/COMMIT-REQUEST.md)
- [`templates/PR-REQUEST.md`](templates/PR-REQUEST.md)

---

## Reader outcome

学完这个模块后，你应该能把一句模糊要求改写成可复用的执行合同，让 agent 的行为更稳定。

---

## ⏭️ 建议下一步

继续看 [04 - Skills and Agents](../04-skills-and-agents/README.zh-CN.md)。
