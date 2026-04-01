# Commands and Prompts

## Demo case：把一个模糊 docs 任务改写成执行合同

有人只说：“帮我 review 一下这个项目并改进文档。”

把这句话改写成一个明确请求，让 agent 知道要看什么、输出什么、什么时候停。

- [`templates/PLAN-REQUEST.md`](templates/PLAN-REQUEST.md)
- [`templates/REVIEW-REQUEST.md`](templates/REVIEW-REQUEST.md)
- [`templates/COMMIT-REQUEST.md`](templates/COMMIT-REQUEST.md)
- [`templates/PR-REQUEST.md`](templates/PR-REQUEST.md)

请求里明确写出任务类型、真实上下文、约束、输出形状和停止条件。

---

## Step-by-step workflow

1. **先判断任务类型**
   - planning
   - review
   - commit summary
   - PR summary
2. **选对应模板**
3. **补全真实上下文**
   - repo area
   - goal
   - constraints
   - output shape
4. **写清第一步该做什么**
   - 只分析
   - 先出 plan
   - 分析后直接改
5. **写明停止条件**
   - 等批准
   - 只给 draft message
   - 报告后停止
6. **删掉不允许的猜测空间**
   - 不要发明命令
   - 不要发明 issue 编号
   - 不要假设缺失工具已经存在
7. **拿结果和合同对照**
   - 如果输出漂移，就把合同写得更紧
