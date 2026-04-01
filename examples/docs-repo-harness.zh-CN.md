# 文档仓库 Harness 案例

如果你的项目主要是文档和模板，而不是一个已经有完整构建链的应用，就用这个案例。

---

## 第 1 步：先把仓库事实写清楚

在让 OpenCode 重写文档前，先创建或修正 `AGENTS.md`，让 agent 能看到什么是真实的。

最少写清这些：
- 根文档有哪些
- 模块文档有哪些
- 模板有哪些
- 哪些命令仍然是 `TBD`
- 哪些 support docs 已经存在

只要 repo 不能证明命令存在，就不要把它写成真的。

---

## 第 2 步：一次只挑一个文档目标

不要一开始就说“把整个仓库重写掉”。
一次只挑一个目标：
- 根 README
- 某一个模块 README
- 某一个 example 文件
- 某一个 support doc

最好的第一块通常是：
- 把 `README.md` 改成唯一主入口
- 或者把某一个模块改成新手能直接照着做的手册

---

## 第 3 步：先出计划，不要直接改

直接用：
- [../03-commands-and-prompts/templates/PLAN-REQUEST.md](../03-commands-and-prompts/templates/PLAN-REQUEST.md)
- 或 [../.opencode/commands/start-harness-task.md](../.opencode/commands/start-harness-task.md)

要求它先回答：
- 会改哪些文件
- 新结构是什么
- 哪些链接必须保持有效
- 哪些文件应该删掉，而不是继续重写

在 plan 没清楚前，不要让它开始改。

---

## 第 4 步：文档任务要走专门的 review 路径

如果任务主要是文档，不要只用一个泛泛的 review。
把这些一起用：
- [../.opencode/commands/review-docs.md](../.opencode/commands/review-docs.md)
- [../.opencode/commands/review-readme.md](../.opencode/commands/review-readme.md)
- [../.opencode/commands/review-module.md](../.opencode/commands/review-module.md)
- [../.opencode/agents/docs-review.md](../.opencode/agents/docs-review.md)
- [../.opencode/agents/doc-link-checker.md](../.opencode/agents/doc-link-checker.md)
- [../.opencode/agents/repo-facts-checker.md](../.opencode/agents/repo-facts-checker.md)

实际顺序：
1. 先审 wording 和 scope
2. 再审 links 和 navigation
3. 再审 repo facts 还对不对

---

## 第 5 步：根文档按这个顺序改

如果任务会动到根文档，按这个顺序：
1. `README.md`
2. `README.md`
3. `CATALOG.md`
4. `CATALOG.zh-CN.md`
5. 只有确实影响 reporting / contribution / governance 时，再动 support docs

这样最不容易出现根导航漂移。

---

## 第 6 步：把“文档仓库的错误”当成信任问题来查

文档仓库最常见的错误不是代码 bug，而是信任 bug。

每次都检查：
- 发明了不存在的命令
- 还在链接已经删掉的文件
- 中英文入口是否漂移
- 未来计划是否被写成当前事实
- 模板是否夸大了 repo 能力

---

## 第 7 步：没验证前不要停

在你说“这次改完了”之前，至少做这几件事：
1. 跑一次完整 markdown link check
2. 重新读改过的文件，假装自己是第一次来的 contributor
3. 确认删掉或合并的文件不再被引用
4. 如果动了根结构，确认 `README*` 和 `CATALOG*` 还能一起工作

---

## 一套最小可复制流程

如果你的任务是“让这个文档仓库更容易开始使用”，就按这个顺序做：
1. 先更新 `AGENTS.md` 里的事实
2. 把 `README.md` 改成唯一主入口
3. 把完整清单放到 `CATALOG.md`
4. 删掉多余的根介绍文档
5. 跑 `review-docs`
6. 再跑链接校验

---

## 这个案例配合这些文件一起用

- [../README.md](../README.md)
- [../CATALOG.zh-CN.md](../CATALOG.zh-CN.md)
- [../AGENTS.md](../AGENTS.md)
- [../.opencode/README.md](../.opencode/README.md)
