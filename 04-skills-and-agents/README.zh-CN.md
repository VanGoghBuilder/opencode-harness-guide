# Skills 与 Agents

这一章只回答 4 个问题：

1. 什么时候**直接用 OpenCode 内建 agent**
2. 什么时候**创建一个自定义 agent 文件**
3. 什么时候**创建一个自定义 command 文件**
4. 什么时候**创建一个 `SKILL.md`**

如果你只想知道“现在我该建什么文件、怎么写、怎么调”，按下面顺序做。

---

## 先分清 4 种东西

### 1. 内建 agents
官方内建的重点是：
- **primary agents**：`build`、`plan`
- **subagents**：`general`、`explore`

怎么用：
- 切换主 agent：在 OpenCode 会话里用 **Tab** 切换 primary agent
- 手动调用 subagent：在消息里直接写 `@explore` 或 `@general`

例子：
```text
@explore 帮我找一下这个仓库里所有 pricing 相关的实现和文件
```

什么时候直接用内建 agent：
- 只是查代码、读文件、做分析
- 只是想先出 plan，不想改文件
- 只是想把 repo 搜一遍

如果只是这些，不要先创建新文件。

---

### 2. 自定义 agent
当你需要一个**长期复用的角色**时，再建 agent。

适合建 agent 的情况：
- 你反复做同一类工作，例如 `docs-review`、`security-audit`
- 你希望这个角色总是用同样的语气、边界和权限
- 你希望它能被 `@名字` 直接调用

要创建什么文件：
- 项目内：`.opencode/agents/<name>.md`
- 全局：`~/.config/opencode/agents/<name>.md`

最小例子：创建 `.opencode/agents/docs-review.md`

```md
---
description: 审查文档是否与仓库现实一致
mode: subagent
permission:
  edit: deny
  bash: deny
---
你是一个文档审查 agent。
只做这些事：
- 检查是否发明了不存在的命令
- 检查 present facts 和 future plans 是否混在一起
- 检查 README / INDEX / CATALOG 是否同步
不要修改文件，只给出问题列表。
```

怎么调用：
```text
@docs-review 帮我检查这次 README 改动有没有发明不存在的命令
```

如果你不想手写，也可以直接运行官方命令：
```bash
opencode agent create
```
它会交互式帮你创建 agent 文件。

---

### 3. 自定义 command
当你已经有一个**经常重复的用户入口动作**时，再建 command。

适合建 command 的情况：
- 你每次都输入一大段类似 prompt
- 你想在 TUI 里直接敲 `/xxx`
- 你想把固定模板绑定到一个 agent 或当前 agent

要创建什么文件：
- 项目内：`.opencode/commands/<name>.md`
- 全局：`~/.config/opencode/commands/<name>.md`

最小例子：创建 `.opencode/commands/review-docs.md`

```md
---
description: 审查文档一致性
agent: plan
---
请检查当前仓库文档，重点看：
- 有没有发明不存在的命令
- README / INDEX / CATALOG 是否同步
- present facts 和 future plans 是否分开
只输出问题列表，不要改文件。
```

怎么调用：
```text
/review-docs
```

如果要传参数，可以这样写：

```md
---
description: 审查指定文件的文档一致性
agent: plan
---
请审查 $ARGUMENTS 这个文件，检查：
- 是否发明命令
- 是否与仓库现实冲突
- 是否需要更新导航
```

调用时：
```text
/review-docs README.md
```

重点记住：
- **command 是用户入口**
- **agent 是执行角色**
- command 可以绑定 agent

---

### 4. Skill (`SKILL.md`)
当很多 agent 都要按同一套步骤做事时，再建 skill。

适合建 skill 的情况：
- 不是固定角色，而是一套固定步骤
- 这套步骤会被多个 agent 一起用
- 你不想每次都重新写同一套规则

官方要求你创建这样的文件结构：
- 项目内：`.opencode/skills/<name>/SKILL.md`
- 全局：`~/.config/opencode/skills/<name>/SKILL.md`

最小例子：创建 `.opencode/skills/doc-audit/SKILL.md`

```md
---
name: doc-audit
description: 审查文档是否与仓库现实一致
---
## 什么时候用
当你要检查 README、INDEX、CATALOG、AGENTS 是否一致时使用。

## 执行步骤
1. 先检查是否发明了不存在的命令
2. 再检查 facts / plans 是否混在一起
3. 再检查根导航是否同步
4. 输出问题列表，不直接改文件
```

官方要求注意：
- `name` 必须和目录名一致
- `name` 只能是小写字母、数字和单个 `-`
- `SKILL.md` 文件名必须全大写

怎么调用：
- 对用户来说，一般不是 `/command` 那样直接敲
- skill 是 **agent 通过 `skill` 工具加载** 的
- 你通常会在提示词里要求：
  - “先加载 `doc-audit` skill，再做检查”
  - 或者让 agent 自己发现并加载

内部调用方式长这样：
```text
skill({ name: "doc-audit" })
```

你作为用户，更实用的说法是：
```text
先加载 doc-audit skill，然后检查 README 和 INDEX 是否一致。
```

---

## 现在到底该选哪一种？

按这个顺序判断：

### 只想先做一次
不要建任何文件。
直接：
- 用 `plan` / `build`
- 或者 `@explore` / `@general`

### 我总是要重复打一段 prompt
建：
- `.opencode/commands/<name>.md`

### 我需要一个固定角色，能反复 `@名字` 调用
建：
- `.opencode/agents/<name>.md`

### 很多 agent 都要按同一套步骤做事
建：
- `.opencode/skills/<name>/SKILL.md`

---

## 一个最实用的入门顺序

如果你现在是第一次整理这块，按这个顺序做：

1. **先不要建 skill，也不要建 agent**
2. 先建一个 command：
   - `.opencode/commands/review-docs.md`
3. 连续用 3 到 5 次
4. 如果你发现“不是 prompt 在重复，而是角色在重复”，再建 `.opencode/agents/docs-review.md`
5. 如果你发现“不是角色在重复，而是方法在重复”，再把方法提炼成 `.opencode/skills/doc-audit/SKILL.md`

这样最稳，不容易一上来就把系统搞复杂。

---

## 直接照做的最小实践

### 目标：给你的项目增加一个“文档审查入口”

#### 第一步：创建 command 文件
创建：
- `.opencode/commands/review-docs.md`

内容：
```md
---
description: 审查文档一致性
agent: plan
---
请检查当前仓库文档，重点看：
- 有没有发明不存在的命令
- README / INDEX / CATALOG 是否同步
- present facts 和 future plans 是否分开
只输出问题列表，不要改文件。
```

#### 第二步：在 OpenCode 里运行
```text
/review-docs
```

#### 第三步：如果你总是需要更深的 repo 搜索
直接在消息里加：
```text
@explore 帮我找出所有和 README 导航相关的文件
```

#### 第四步：如果这个流程稳定复用很多次
再创建：
- `.opencode/agents/docs-review.md`

#### 第五步：如果最后你发现复用的是“方法”而不是“角色”
再创建：
- `.opencode/skills/doc-audit/SKILL.md`

---

## 直接看这些官方文档

- Agents: <https://opencode.ai/docs/agents/>
- Commands: <https://opencode.ai/docs/commands/>
- Agent Skills: <https://opencode.ai/docs/skills/>
- Tools: <https://opencode.ai/docs/tools/>

---

## 这个仓库里你可以直接参考的文件

- [templates/SPECIALIZATION-DECISION-CHECKLIST.md](templates/SPECIALIZATION-DECISION-CHECKLIST.md)
- [templates/skills/self-assessment/SKILL.md](templates/skills/self-assessment/SKILL.md)
- [templates/skills/self-assessment/README.md](templates/skills/self-assessment/README.md)

