# Cross-Stack Templates

> **Harness 职责**：这个模块帮助你让 harness 跨技术栈迁移，而不发明不存在的工具链。

这个模块讨论哪些 OpenCode harness 模式是通用的，什么时候 stack-specific starter 才算真的成立。

---

## 为什么这很重要

harness 应该可迁移，但不能“假装可迁移”。
通用层要能跨 repo 复用，而 stack-specific 层必须等真实文件和真实命令存在之后再写。

---

## 🧭 这个模块适合谁

如果你有这些需求，就读这一章：
- 在多个语言或框架之间工作
- 想知道哪些 harness 模式是 universal 的
- 容易过早写 stack-specific guide

---

## ⏱️ 15 分钟内你能完成什么

读完之后，你应该能：
1. 区分 universal harness patterns 和 stack-specific details
2. 审查一个 stack starter 是否真的 ready
3. 防止 docs 里出现假 portability

---

## 这个模块假设什么，不假设什么

这个模块假设：
- 你可能想把当前 harness 思路迁移到别的 repo

这个模块不假设：
- 当前 repo 已经选定 stack
- stack-specific commands 已经 verified

---

## 🧠 Universal vs stack-specific harness layers

通用 harness 层通常包括：
- repo context
- execution contracts
- capability routing
- automation boundaries
- feedback 和 review 习惯

stack-specific 层通常包括：
- 具体命令
- formatter 名称
- build pipeline
- framework-specific 结构

---

## Demo case：一个 Next.js starter harness 现在真的 ready 吗？

### Situation
你想写一份 “Next.js + OpenCode harness starter”，但当前仓库里没有 verified `package.json`、没有 lint script，也没有 build command。

### Goal
避免写出一份 fake starter kit。

### Desired result
通用 harness 层先独立发布，stack-specific 部分继续标记为 not ready。

### Micro-example
- 现在就能保留：`AGENTS.md`、facts checklist、planning / review contracts
- 应该移到 `TBD`：`npm run lint`、`npm test`、framework-specific build steps、没有文件证据的 starter kit 声明

---

## 🛠️ Step-by-step workflow

1. **列出 universal harness 部分**
   - `AGENTS.md`
   - facts checklist
   - planning / review contracts
2. **列出你想写的 stack-specific claims**
3. **要求每个 claim 都有文件证据**
4. **保留 verified 的部分**
5. **把其他内容放进 `TBD` 或 future work**
6. **先发布 universal layer，不要为了等 stack 而把一切都拖住**

---

## 常见失败模式与修复

### 失败模式 1：从别的 repo 复制 stack guide，然后假设这里也成立
修复：每个命令都回到真实文件验证。

### 失败模式 2：把“措辞可复用”误当成“系统可迁移”
修复：把 universal patterns 和 stack-bound details 分开写。

### 失败模式 3：因为 stack 还没定，所以什么都不写
修复：先把 universal harness 层写出来。

---

## Starter asset

使用：
- [`templates/STACK-STARTER-READINESS-CHECKLIST.md`](templates/STACK-STARTER-READINESS-CHECKLIST.md)

---

## Reader outcome

学完这个模块后，你应该能判断一个 harness 的哪一层能立刻复用，哪一层必须等 stack 事实出现后再写。

---

## ⏭️ 建议下一步

继续看 [09 - Advanced Workflows](../09-advanced-workflows/README.zh-CN.md)。
