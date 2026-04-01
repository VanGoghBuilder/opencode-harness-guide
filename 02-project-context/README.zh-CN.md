# 项目上下文

## 演示案例：把 repo audit 变成 system of record

一个仓库有文档、有目录、可能还有 `.github/`，但没有明显 build system，也没有明确命令说明。用 [`templates/PROJECT-FACTS-CHECKLIST.md`](templates/PROJECT-FACTS-CHECKLIST.md) 审计仓库，只把已验证事实写进 `AGENTS.md`，其余内容继续标成 `TBD`、not yet present 或 future direction。

---

## 操作步骤

1. **打开 checklist**
   - 不要凭记忆填写
2. **按类别逐项检查**
   - core files
   - stack files
   - commands
   - conventions
3. **每一项都要求证据**
   - 文件真的存在吗？
   - 配置真的存在吗？
   - 命令真的有定义吗？
4. **把每项分到 3 个桶里**
   - verified fact
   - `TBD` / not yet present
   - future direction
5. **只把已验证的内容写进 `AGENTS.md`**
6. **把缺失内容显式写出来**
   - 用 `TBD` 或 `Not yet present`
7. **让 checklist 和 `AGENTS.md` 保持同步**
