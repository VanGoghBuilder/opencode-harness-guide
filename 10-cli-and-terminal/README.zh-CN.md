# CLI and Terminal Usage（中文版）

> **Harness 职责**：这个模块定义人类意图、OpenCode、plugins 与系统 shell 之间的执行边界。

**语言 / Language：** [简体中文](README.zh-CN.md) | [English](README.md)

这个模块讨论如何诚实地记录命令、如何理解终端边界，以及何时应该把命令文档继续保持在 `TBD`。

---

## 🧭 这个模块适合谁

如果你关心这些事情，就读最后一章：

- 你想在命令行或终端界面里使用 OpenCode
- 你想在脚本、CI/CD 或本地 shell 中调用它
- 你想理解 OpenCode 代你执行 shell 命令时，边界在哪里

---

## ⏱️ 15 分钟内你能完成什么

读完之后，你应该能：

1. 理解 OpenCode 的 CLI 和系统 shell 之间的边界
2. 更安全地让代理使用终端能力
3. 为团队写出更真实的命令文档

---

## 🧠 OpenCode 与终端

OpenCode 和终端的关系，通常可以从两个角度理解：

1. **作为界面**：你运行 `opencode`（或对应 CLI）来进行对话
2. **作为执行者**：OpenCode 通过 `bash` 等工具去执行命令

```mermaid
graph LR
    A["开发者"] -->|运行 CLI| B["OpenCode 界面"]
    B -->|代理决定| C["Bash 工具"]
    C -->|执行| D["系统 Shell"]
    D -->|返回输出| C
    C -->|解析| B
    B -->|反馈| A
```

### 安全与边界

- OpenCode 会在当前工作目录运行命令
- 尽量不要用 `cd <dir> && <command>`，而是明确指定 `workdir`
- 高风险命令（例如 `git push --force`）必须有用户明确同意
- 带交互提示的命令如果处理不当，很容易卡住

---

## 🛠️ 动手练习：记录已验证命令

一个常见错误，是把“未来可能会有的命令”写进文档，结果同时误导人和代理。

### 练习步骤

1. 打开你项目里的 `AGENTS.md` 或命令文档
2. 查看 Install、Lint、Test、Build 这些部分
3. 在终端里按文档所写逐条手动执行
4. 如果跑不通，就把文档改回 `TBD`
5. 不要发明命令；仓库真实用什么，就写什么

> **核心规则**：终端文档必须反映现实，而不是愿景。

---

## 🎉 总结

你已经走完这个仓库当前的核心 Harness 路径。现在你应该已经能把 OpenCode 锚定在现实里，使用结构化执行合同，理解技能和代理，判断自动化边界，并以更真实的方式定义命令与终端边界。

如果你要查产品级功能细节，还是应该回到 [OpenCode 官方文档](https://opencode.ai/docs/)。

- [返回学习路线图](../LEARNING-ROADMAP.zh-CN.md)
- [查看中文目录](../CATALOG.zh-CN.md)
