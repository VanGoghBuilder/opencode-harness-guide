# CLI and Terminal Usage

## Demo case：审计一个命令区块是否诚实

一个 repo 文档列出了 install、lint、test、build 等命令，但仓库里未必真的有支撑这些命令的文件。把这段命令文档改成“反映现实”，让新 contributor 能一眼看出哪些命令已验证、哪些缺失、哪些仍是 `TBD`，同时把 shell safety boundary 写清楚。

---

## Step-by-step workflow

1. **打开命令文档**
   - `AGENTS.md`
   - README 里的 command section
   - 其他 stack notes（如果有）
2. **列出每个声称存在的命令**
   - install
   - lint
   - test
   - typecheck
   - build
3. **问：哪个文件能证明它存在？**
   - package manifest
   - Makefile
   - CI config
   - tool config with documented script path
4. **给每个命令分类**
   - verified
   - not yet present
   - `TBD`
5. **按分类重写文档**
6. **重写时顺手检查 shell safety boundary**
   - OpenCode 会在当前工作目录运行命令
   - 优先使用显式 `workdir`，而不是 `cd && ...`
   - destructive commands 需要明确用户同意
   - interactive commands 需要特殊处理
   - 不要混淆 built-in behavior 和 plugin behavior
7. **继续显式记录缺失**
   - 诚实的 `TBD` 比伪造命令更好
   - 标明命令是 local-only、CI-only，还是 generally usable
