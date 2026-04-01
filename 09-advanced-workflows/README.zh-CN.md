# Advanced Workflows

## Demo case：把一个薄弱模块 README 扩成真正的 harness playbook

一个模块 README 概念是对的，但只有一个很短的 exercise，没有 worked demo。用 [`templates/ADVANCED-WORKFLOW-CHECKLIST.md`](templates/ADVANCED-WORKFLOW-CHECKLIST.md) 和 [`templates/OMO-VIBE-CODING-KICKOFF.md`](templates/OMO-VIBE-CODING-KICKOFF.md) 把它改写成一个围绕真实 demo case 的可执行 playbook，并把边界写清楚。

---

## Step-by-step workflow

1. **先看当前状态**
   - 读模块
   - 读相关模板
   - 看根导航希望它承担什么角色
2. **定义改写目标**
   - 这个模块要防止哪类失败？
   - 读者读完后应该会做什么？
3. **设置 planning gate**
   - 先列出改写结构
4. **围绕一个 demo case 重写**
   - situation
   - goal
   - artifacts
   - steps
   - failure modes
5. **把边界写实，不要混写**
   - 内部扩展行为归 plugins
   - 外部系统归 MCP
   - 更强社区编排归 oh-my-opencode
   - stop condition 不清楚就回 planning
6. **验证 links、file references 和 claims**
7. **再做一轮 clarity review**
