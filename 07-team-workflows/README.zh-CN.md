# Team Workflows

> **Harness 职责**：这个模块让 harness 不只对一个操作者有效，而能长期支持团队协作。

这个模块讨论 onboarding、共享约定，以及如何让团队文档始终和仓库现实保持一致。

---

## 为什么这很重要

如果一套 harness 只对一个人有效，那它本质上只是个人习惯，而不是团队系统。
真正可靠的团队协作，要求 repo 本身承载规则，而不是靠口头传承。

---

## 🧭 这个模块适合谁

如果你正在做这些事情，就读这一章：
- 把 OpenCode 引入团队
- 不想让每个 teammate 都发明自己的 workflow
- 想让新 contributor 不靠猜就能开始工作

---

## ⏱️ 15 分钟内你能完成什么

读完之后，你应该能：
1. 说清什么属于 repo、什么应该留在本地
2. 审查 onboarding readiness
3. 找出并修掉一个依赖 tribal knowledge 的缺口

---

## 这个模块假设什么，不假设什么

这个模块假设：
- 除了你之外，还会有其他人使用这个 repo
- 一部分 workflow 知识目前还停留在脑子里

这个模块不假设：
- repo 的 onboarding 文档已经完善
- 所有本地 setup 都适合提交进仓库

---

## 🧠 Shared harness vs private habit

团队 harness 是能穿越人员变动、记忆丢失和工具变更的那一层。
应该写进 repo 的，必须写进 repo；应该留在本地的，不要为了“方便”就提交进去。

---

## Demo case：只靠 repo 文档 onboarding 一个新 contributor

### Situation
一个新 contributor 需要更新一个模块 README，并保持导航和事实边界一致。

### Goal
验证 TA 是否能在不问同事的情况下完成任务。

### Artifacts in play
- `AGENTS.md`
- `README.md`
- `INDEX.md`
- `CATALOG.md`
- [`templates/TEAM-ONBOARDING-CHECKLIST.md`](templates/TEAM-ONBOARDING-CHECKLIST.md)

### Desired result
你能明确看到：repo 里还有哪些规则其实还藏在私有记忆里。

---

## 🛠️ Step-by-step workflow

1. **挑一个真实 newcomer task**
2. **只依赖 repo 文档尝试完成**
3. **记录每一个必须靠外部帮助的地方**
4. **给每个缺口分类**
   - missing rule
   - missing navigation
   - missing template
   - missing support doc link
5. **修补 repo，而不是接受记忆缺口**
6. **过一段时间换另一个任务再测一次**

---

## 什么应该进 repo

- harness 规则与 repo facts
- 共享 execution contracts
- plugin 与 integration 指南
- team-readable onboarding notes

## 什么应该留在本地

- secrets 和 tokens
- 个人偏好配置
- 机器专属私有数据

---

## 常见失败模式与修复

### 失败模式 1：说“有问题来问我”
修复：把缺失规则写进 repo。

### 失败模式 2：为了 onboarding 方便而提交 secrets
修复：记录 setup 形状，不记录 secret value。

### 失败模式 3：一次 onboarding 成功就以为 harness 完整了
修复：换另一类任务再测试一次。

---

## Starter asset

使用：
- [`templates/TEAM-ONBOARDING-CHECKLIST.md`](templates/TEAM-ONBOARDING-CHECKLIST.md)

---

## Reader outcome

学完这个模块后，你应该能找出并修掉 repo 里至少一个 tribal knowledge 缺口。

---

## ⏭️ 建议下一步

继续看 [08 - Cross-Stack Templates](../08-cross-stack-templates/README.zh-CN.md)。
