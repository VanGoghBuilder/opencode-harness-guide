# .opencode Starter Pack 中文说明

如果你想把这套 OpenCode starter files 直接复制到真实项目里，就看这个文件。

复制时要保留同样的 `.opencode/` 目录结构，不要把文件散着放。

---

## 里面有什么

- `commands/review-docs.md`
- `commands/review-readme.md`
- `commands/review-module.md`
- `commands/start-harness-task.md`
- `agents/docs-review.md`
- `agents/doc-link-checker.md`
- `agents/harness-planner.md`
- `agents/repo-facts-checker.md`
- `skills/doc-audit/SKILL.md`

这些 starter files 目前仍主要是英文，因为它们本来就是给 OpenCode 直接读取和执行的样例。

---

## 最稳的使用顺序

1. 先复制 `commands/review-docs.md`
2. 如果你想专门检查根 README，再复制 `commands/review-readme.md`
3. 如果你想专门检查某个模块，再复制 `commands/review-module.md`
4. 如果你发现自己需要固定角色，再复制一个 agent
5. 如果多个 agent 都要按同一套步骤做事，再复制 skill

---

## 什么时候先不要复制

如果你的 repo 里这些事还没写清楚，就先不要复制 starter pack：
- `AGENTS.md` 还没写
- repo facts 还没整理
- 命令是否存在还没核对

先把这些基础做好，再复制 `.opencode` 文件。
