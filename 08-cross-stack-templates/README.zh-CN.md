# Cross-Stack Templates

## Demo case：一个 Next.js starter harness 现在真的 ready 吗？

你想写一份 `Next.js + OpenCode harness starter`，但当前仓库里没有 verified `package.json`、没有 lint script，也没有 build command。用 [`templates/STACK-STARTER-READINESS-CHECKLIST.md`](templates/STACK-STARTER-READINESS-CHECKLIST.md) 只发布已经可验证的通用 harness 层，把没有文件证据的 stack-specific 声明继续留在 `TBD` 或 future work。

---

## Step-by-step workflow

1. **列出 universal harness 部分**
   - `AGENTS.md`
   - facts checklist
   - planning / review contracts
2. **列出你想写的 stack-specific claims**
3. **要求每个 claim 都有文件证据**
4. **保留 verified 的部分**
5. **把其他内容放进 `TBD` 或 future work**
6. **先发布 universal layer**
