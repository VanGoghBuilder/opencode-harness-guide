# Vibe Coding 与 oh-my-opencode 实战

当你不想再用自由聊天撞运气，而是想把任务放进一个更强的工程 harness 里时，就看这个文件。

---

## 5 步执行循环

### 1. 先把 repo 地图站稳
在你要求改代码之前：
- 确保 `AGENTS.md` 存在
- 确保 repo facts 是新的
- 确保缺失命令仍然写成 `TBD`

如果地图是错的，整场 session 都会漂。

### 2. 从 kickoff 开始，不要从模糊请求开始
直接用 [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)。

第一条消息要强制做到：
- 并行探索
- 实现前先出 plan
- 约束明确
- 有 stop condition

### 3. 一定要过 planning gate
不要让 agent 一上来就编辑文件。
先要求它给出：
- 会改哪些文件
- 打算怎么改
- 有哪些 edge cases
- 后面准备怎么验证

plan 错了，就在这里改，不要等代码写下去后再返工。

### 4. 把任务路由给正确能力
不要把所有事都塞进一个大对话里。
按任务类型拆：
- UI → `visual-engineering`
- 硬逻辑 → `ultrabrain`
- 外部参考 → `librarian`
- repo 搜索 → `explore`

### 5. 没验证前，不要接受结果
要求：
- 对改过的文件跑 `lsp_diagnostics`
- 如果 repo 定义了真实命令，就跑真实命令验证
- 对高风险逻辑做 review

如果 repo 没有 verified build / test 命令，就不要假装有。

---

## 一个实际例子

### 任务
“给一个 Next.js SaaS 应用加 pricing page。”

### 更好的 harness 流程
1. 先看 [examples/nextjs-saas-harness.zh-CN.md](examples/nextjs-saas-harness.zh-CN.md)
2. 用 kickoff template 强制进入 analysis mode
3. 要求它先给页面、数据源和验证方案的 plan
4. UI 路由给 `visual-engineering`
5. Stripe / server 逻辑路由给逻辑更强的 agent
6. 只有 diagnostics 和 build 过了，才接受结果

---

## 如果 session 开始跑偏

### 症状：agent 太早开始写代码
动作：停下来，要求先出 plan。

### 症状：agent 开始猜命令
动作：回到 `AGENTS.md` 和 facts checklist。

### 症状：一个 chat 想包打一切
动作：按 capability 重新拆分任务。

### 症状：结果“听起来没问题”，但没有验证
动作：在接受前要求 diagnostics 或其他真实检查。

---

## 这几个文件要一起看

- [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md)
- [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)
- [examples/nextjs-saas-harness.zh-CN.md](examples/nextjs-saas-harness.zh-CN.md)
