# Skills and Agents

## Demo case：一个重复的 docs 任务要不要做成 skill？

你反复要求 agent 做 docs 审计：检查 broken assumptions、导航是否同步、present-vs-planned wording 是否漂移。用 [`templates/SPECIALIZATION-DECISION-CHECKLIST.md`](templates/SPECIALIZATION-DECISION-CHECKLIST.md) 判断这个任务更适合继续做 prompt、升格成 skill，还是拆给专门 agent，而不是盲目增加复杂度。

---

## Step-by-step workflow

1. **先给重复任务命名**
   - 例如：`doc consistency audit`
2. **判断真正重复的部分**
   - instructions
   - decision rules
   - search pattern
   - review boundary
3. **选择最轻的有效路由**
   - prompt first
   - skill second
   - agent when role boundary or tooling boundary matters
4. **用一个真实任务试跑**
5. **检查它有没有真的减少 guesswork**
6. **只有收益真实时，才提升复杂度**
