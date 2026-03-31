# Next.js SaaS Harness — OpenCode Harness 案例

> 这是一个将 OpenCode Engineering Harness（工程脚手架）应用于 Next.js + Supabase + Stripe SaaS 项目的实战案例。
> 复制此结构到你的项目根目录，让你的 Agent 锚定在真实的开发环境中。

## 1. 地图层 (`AGENTS.md`)

这是你最小的 Harness 入口点。它告诉 Agent 什么是真实的，以及需要遵守什么规则。

```markdown
# 仓库 Harness 上下文

- **技术栈**: Next.js 15 (App Router), TypeScript, Supabase (Auth + DB), Stripe (Billing), Tailwind CSS
- **架构**: 默认使用 Server Components。只在需要交互的地方使用 Client Components。
- **状态**: 绿地项目，基础脚手架已存在，`npm run dev` 运行正常。

## 关键 Harness 规则

### 数据库与鉴权
- 所有查询必须使用开启了 RLS 的 Supabase 客户端。严禁绕过 RLS。
- 迁移文件放在 `supabase/migrations/`。不要通过 SQL 提示直接修改数据库。
- 在 Server Components 中使用 `@supabase/ssr` 的 `createServerClient()`。

### 代码风格与约束
- 仅使用不可变模式（Immutable patterns）：使用展开运算符，绝对不要直接改变对象。
- Server Components: 禁止使用 `'use client'` 指令，禁止使用 `useState`/`useEffect`。
- 所有 API 路由和表单输入验证优先使用 Zod schemas。

### 自动化边界
- 在声称任务完成前，`npm run lint` 和 `npm run build` 必须通过。
- 不要自动合并 PR。
```

## 2. 执行合同 (`PLAN-REQUEST.md`)

当你希望 Agent 开发新功能（例如添加定价页面）时，使用此合同，而不是模糊的提示词。

```markdown
# Harness 执行合同

[analyze-mode]
ANALYSIS MODE. Gather context before diving deep:

CONTEXT GATHERING (parallel):
- 派发 1-3 个 `explore` agent 去梳理 `src/lib/stripe/` 中当前的 Stripe 计费实现。
- 派发 1 个 `librarian` agent 去查阅最新的 Next.js 15 Server Action 模式（如果需要）。

SYNTHESIZE findings before proceeding. Present a concrete plan (files to modify, components to create, API routes needed).

DO NOT START IMPLEMENTING UNTIL I APPROVE THE PLAN.

---

### 🎯 意图
实现 `/pricing` 页面，展示 3 个层级（Free, Pro, Enterprise），并从 Stripe 获取动态价格数据。

### 📋 约束
- 在服务端获取价格。永远不要信任客户端的价格数据。
- 使用 Shadcn/ui 组件制作定价卡片。
- 确保实现后 `lsp_diagnostics` 没有报错。
```

## 3. 反馈回路与验证

不要盲目接受代码。运行验证循环。

1. **诊断**: 要求 Agent 对所有修改过的文件运行 `lsp_diagnostics`。
2. **构建**: 要求 Agent 运行 `npm run build` 以捕捉 Server/Client 组件的边界错误。
3. **评审**: 如果逻辑复杂，使用评审合同：

```markdown
# 评审合同

请评审 `app/api/webhooks/stripe/route.ts` 中新添加的 Stripe webhook 处理器。

- 它是否正确验证了 Stripe 签名？
- 它是否以不可变的方式处理了 `checkout.session.completed` 事件？
- 是否有任何暴露的 secrets 或未处理的错误？
```

## 4. 能力路由

不要在一个对话里做所有事情，对工作进行路由分发：
- **UI 调整**: 路由给 `visual-engineering` 子代理，用 Tailwind 设定定价卡片样式。
- **计费逻辑**: 路由给 `ultrabrain` 子代理，处理 webhook 解析和数据库更新。
- **外部文档**: 使用 `librarian` 查找准确的 Stripe API payload 格式。

## 5. 集成与 MCP (`LOCAL-INTEGRATION-NOTES.md`)

安全地记录外部依赖，这样团队就可以使用 harness 而不泄露 secrets。

```markdown
# 外部能力需求

此项目使用 MCP 进行数据库检查和 GitHub Issue 追踪。

- **Supabase DB**: 使用 Postgres MCP server。
  - 需要环境变量: `POSTGRES_CONNECTION_STRING` (绝对不要提交这个！)
  - 范围: 只读访问，用于验证迁移是否正确应用。
- **GitHub**: 使用 GitHub MCP server 读取功能请求。
  - 需要环境变量: `GITHUB_PERSONAL_ACCESS_TOKEN`
```
