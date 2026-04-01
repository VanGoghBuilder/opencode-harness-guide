# 开始搭建 Harness

## 演示案例：你接手一个“半空白”仓库的前 15 分钟

你打开一个仓库，能看到 `README.md`、几个目录、一些文档，但没有明显的 package manifest，也没有命令说明。使用 [`templates/AGENTS.md`](templates/AGENTS.md) 给这个仓库建立一个最小可用的 harness 入口，让 agent 停止猜测。完成后，仓库里应该出现一个 starter `AGENTS.md`，明确说明现在真实存在什么、现在还没有什么，以及 agent 不应该发明什么。

---

## 操作步骤

1. **先看根目录**
   - 先列出顶层文件和目录
   - 只记录已经存在的内容
2. **把事实和猜测分开**
   - 只有真实文件能支持的内容才算事实
   - 其余内容都先当成未验证
3. **把未知项写成 `TBD`**
   - 仓库没证明的内容都先写成 `TBD`
4. **复制 starter `AGENTS.md`**
   - 从 [`templates/AGENTS.md`](templates/AGENTS.md) 开始
5. **把占位内容替换成真实仓库事实**
   - 已存在的文件和目录
   - 缺失的工具链或命令
   - 已经写明的项目方向
6. **加上一条安全默认规则**
   - 直接写：`Do not invent commands that no file defines.`
7. **再读一遍，假装自己是 agent**
   - 确认能看懂现在有什么
   - 确认能看懂哪些还没有
   - 确认不会被诱导去猜
