# Hooks 与自动化

## 演示案例：给这个 docs-first repo 分类重复检查

这个仓库没有 verified package manager，也没有 test suite，但它确实有很多重复的文档完整性检查。用 [`templates/AUTOMATION-BOUNDARY-CHECKLIST.md`](templates/AUTOMATION-BOUNDARY-CHECKLIST.md) 判断哪些检查现在该自动化，哪些应该继续手动处理。

---

## 操作步骤

1. **列出重复任务**
2. **分 3 个桶**
   - automate now
   - keep manual
   - candidate only
3. **只自动化有证据、结果明确的检查**
   - markdown link validation
   - 根导航漂移检查
   - secret 暴露检查
   - 确保未验证命令继续写成 `TBD`
4. **把主观或不受支持的工作留给人工**
   - broad quality judgments
   - subjective content review
   - auto-merge 行为
   - 任何依赖未验证 tooling 的流程
5. **把官方边界写清楚**
   - plugins 写成扩展层
   - hooks 写成扩展层里的自动化触发点
6. **把这条边界写进 repo，让后续 agent 能看到**
   - 对存在与不存在的内容都保持诚实
