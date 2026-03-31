# Skills and Agents

> **Harness 职责**：这个模块帮助你把任务路由到正确能力边界，而不是所有事都混着处理。

这个模块解释：什么时候一个 prompt contract 就够了，什么时候应该使用 skill，什么时候应该把任务交给 agent。

---

## 为什么这很重要

很多 agent 系统不稳定，并不是因为“能力不够”，而是因为所有任务都被当成同一种任务处理。
有些任务只需要一个 prompt，有些任务需要 skill，有些则需要专门 agent 去承担不同的 reasoning role。

这个模块就是能力路由（capability routing）。

---

## 🧭 这个模块适合谁

如果你有这些问题，就看这一章：
- 某类工作在 repo 里反复出现
- 你想让探索、规划、评审行为更稳定
- 你不确定该继续写 prompt，还是应该升格成 skill / agent

---

## ⏱️ 15 分钟内你能完成什么

读完之后，你应该能：
1. 解释 prompt contract、skill、agent 的区别
2. 为一个重复任务选择更合理的 routing strategy
3. 避免过早专业化

---

## 这个模块假设什么，不假设什么

这个模块假设：
- 你已经懂 repo context 和执行合同
- 你已经开始看到重复模式

这个模块不假设：
- 每个重复任务都值得做 skill
- 每个困难问题都需要新 agent
- 社区插件工作流能替代原生 OpenCode 能力

---

## 🧠 一个实用 routing 模型

可以用这个顺序：
- **Prompt contract**：任务局部、结构清楚，光靠合同就够
- **Skill**：任务反复出现，而且每次都需要相似的专业指令
- **Agent**：任务需要独立的 reasoning role、搜索方式或质量边界

这就是 harness 里的 capability routing。

---

## Demo case：一个重复的 docs 任务要不要做成 skill？

### Situation
你反复要求 agent 去做 docs 审计：检查 broken assumptions、导航是否同步、present-vs-planned wording 是否漂移。

### Better question
重复的到底是什么？
- wording？
- decision rules？
- search behavior？
- review boundary？

这决定了它更适合继续做 prompt、升格成 skill，还是直接交给 agent。

### Artifacts in play
- 一个重复出现的 repo 任务
- 一份现有 prompt contract
- 一个候选的 skill 或 agent 路由

### Desired result
你能解释为什么这个任务应该继续做 prompt、升格成 skill，或交给专门 agent，而不是盲目增加复杂度。


---

## 🛠️ Step-by-step workflow

1. **先给重复任务命名**
2. **判断真正重复的部分**
   - instructions
   - rules
   - search pattern
3. **选择最轻的有效路由**
   - prompt first
   - skill second
   - agent when role boundary matters
4. **用一个真实任务试跑**
5. **看它是否真的减少了 guesswork**
6. **只有收益真实时，才提升复杂度**

---

## 常见失败模式与修复

### 失败模式 1：本来只需要更好的 prompt，却做了一个 skill
修复：先强化执行合同。

### 失败模式 2：小任务也用昂贵或高度专业 agent
修复：把 routing 往下调，不要默认往上加系统。

### 失败模式 3：把社区插件工作流和 OpenCode 原生能力混为一谈
修复：把 capability boundary 单独写清楚。

---

## Starter assets

使用：
- [`templates/SPECIALIZATION-DECISION-CHECKLIST.md`](templates/SPECIALIZATION-DECISION-CHECKLIST.md)
- [`templates/skills/self-assessment/README.md`](templates/skills/self-assessment/README.md)

---

## Reader outcome

学完这个模块后，你应该能判断一个重复任务应该继续保持为 prompt、升格成 skill，还是交给 agent。

---

## ⏭️ 建议下一步

继续看 [05 - Hooks and Automation](../05-hooks-and-automation/README.zh-CN.md)。
