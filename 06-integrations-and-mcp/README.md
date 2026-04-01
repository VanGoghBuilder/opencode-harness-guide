# 集成与 MCP

## 演示案例：记录一个安全的 GitHub 集成，而不泄露 token

团队希望 OpenCode 通过 MCP server 去读取 PR 和 issue 元数据，同时不把任何真实 token 提交进仓库。用 [`templates/LOCAL-INTEGRATION-NOTES.md`](templates/LOCAL-INTEGRATION-NOTES.md) 只记录 setup 形状和安全边界，让团队成员能按说明完成集成，而不会暴露凭证，也不会给 server 过大的权限。

---

## 操作步骤

1. **先命名外部系统**
   - 例如：GitHub
2. **先判断这里是不是真的需要 MCP**
   - built-in tools 已经够用时先用 built-in tools
   - 需要更强内部扩展行为时看 plugins
   - 需要接本地工具面之外的外部系统时再用 MCP
3. **只记录 setup envelope**
   - server 名称
   - env var 名称
   - 权限范围
4. **写清安全边界**
   - read-only 还是 write-capable
   - 高风险动作是否需要人工确认
5. **把 secrets 留在 repo 外**
   - 不要提交 secret value
   - 使用环境变量或本地配置
   - 保持最小权限
6. **共享说明，不共享凭证**
