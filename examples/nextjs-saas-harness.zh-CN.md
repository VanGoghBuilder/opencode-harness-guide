# Next.js SaaS Harness 案例

如果你的项目长得像一个典型 SaaS 应用，并且你想要的是一套可执行的 OpenCode harness，而不是泛泛建议，就直接照这个案例做。

---

## 第 1 步：先写 repo 入口

在项目根目录创建 `AGENTS.md`，把 agent 不允许猜的事实写进去。

```markdown
# Repository Harness Context

- Stack: Next.js 15 (App Router), TypeScript, Supabase (Auth + DB), Stripe (Billing), Tailwind CSS
- Architecture: Server Components by default. Client Components only for interactivity.
- 当前已验证命令: `npm run dev`、`npm run lint`、`npm run build`

## Hard rules
- 所有查询都使用开启 RLS 的 Supabase。
- 迁移文件放在 `supabase/migrations/`。
- 永远不要信任客户端价格数据。
- Server Components: 不要用 `'use client'`、`useState`、`useEffect`。
- 在接受改动前，`npm run lint` 和 `npm run build` 必须通过。
```

先做这个。这个文件如果写错，后面每一步都会变弱。

---

## 第 2 步：用 kickoff contract 启动功能开发

当你要做真实功能时，不要只说“加一个 pricing page”。

用 [../09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](../09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)。下面这段英文可以直接复制，不用翻译后再改。

```markdown
[analyze-mode]
ANALYSIS MODE. Gather context before diving deep:

CONTEXT GATHERING (parallel):
- Fire 1-3 `explore` agents to map the current Stripe billing implementation in `src/lib/stripe/`.
- Fire 1 `librarian` agent to check the latest Next.js 15 Server Action patterns if needed.

SYNTHESIZE findings before proceeding. Present a concrete plan.
DO NOT START IMPLEMENTING UNTIL I APPROVE THE PLAN.

### Intent
实现 `/pricing` 页面，展示 Free / Pro / Enterprise 三档，并使用服务端 Stripe 价格数据。

### Constraints
- 价格必须服务端获取。
- 遵循现有 UI 组件模式。
- 对改动文件运行 `lsp_diagnostics`。
- 在宣布完成前运行 `npm run build`。
```

---

## 第 3 步：按任务类型做路由

不要把 UI、计费逻辑和外部文档查询混在一个大 prompt 里。

这样拆：
- UI 布局和卡片样式 → `visual-engineering`
- billing logic 和 webhook 处理 → 更偏逻辑的 agent，例如 `ultrabrain`
- Stripe API 文档查询 → `librarian`
- repo 内模式搜索 → `explore`

如果一个 prompt 想同时做这四件事，就拆开。

---

## 第 4 步：没验证前不要接受输出

这个类型的应用，按这个顺序验证：

1. 对改动文件运行 `lsp_diagnostics`
2. 运行 `npm run build`
3. 把高风险服务端逻辑单独 review 一次

例如对 Stripe webhook 用一个 review contract：

```markdown
Please review `app/api/webhooks/stripe/route.ts`.

Check:
- Stripe signature verification
- immutable event handling
- missing error handling
- any secret exposure
```

---

## 第 5 步：记录外部能力，但不要泄露 secrets

使用 [../06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](../06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md)。

只记录：
- MCP server 名称
- env var 名称
- 权限范围
- 写操作是否需要确认

例如：

```markdown
- Supabase DB MCP
  - Env var: POSTGRES_CONNECTION_STRING
  - Scope: read-only inspection
- GitHub MCP
  - Env var: GITHUB_PERSONAL_ACCESS_TOKEN
  - Scope: issue and PR reading
```

不要把 token value 提交进仓库。

---

## 第 6 步：如果 session 跑偏了，就回到正确层修

### agent 在出 plan 前就开始写代码
停下来。回到 kickoff contract，要求先出 plan。

### agent 开始猜命令
回到 `AGENTS.md`，修 facts layer。

### 一个任务把 UI、billing、docs lookup 混在一起
按 job type 重新分给不同 agent。

### 输出听起来没问题，但没有验证
在 diagnostics 和 build 过之前，不要接受。

---

## 这个案例要配合这些文件一起用

- [../README.md](../README.md)
- [../09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](../09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)
