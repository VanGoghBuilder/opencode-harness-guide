# Next.js SaaS Harness Case

Use this when your project looks like a typical SaaS app and you want a concrete OpenCode harness instead of general advice.

---

## Step 1: write the repo entry point

Create `AGENTS.md` in the project root and put in the facts that agents must not guess.

```markdown
# Repository Harness Context

- Stack: Next.js 15 (App Router), TypeScript, Supabase (Auth + DB), Stripe (Billing), Tailwind CSS
- Architecture: Server Components by default. Client Components only for interactivity.
- Current verified commands: `npm run dev`, `npm run lint`, `npm run build`

## Hard rules
- All queries use Supabase with RLS enabled.
- Migrations live in `supabase/migrations/`.
- Never trust client-side price data.
- Server Components: no `'use client'`, `useState`, or `useEffect`.
- `npm run lint` and `npm run build` must pass before you accept a change.
```

Do this first. If this file is wrong, every later step gets weaker.

---

## Step 2: start feature work with a kickoff contract

When you want to build a real feature, do not say “add pricing page.” Start with a contract.

Use [../09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](../09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md) and fill it like this:

```markdown
[analyze-mode]
ANALYSIS MODE. Gather context before diving deep:

CONTEXT GATHERING (parallel):
- Fire 1-3 `explore` agents to map the current Stripe billing implementation in `src/lib/stripe/`.
- Fire 1 `librarian` agent to check the latest Next.js 15 Server Action patterns if needed.

SYNTHESIZE findings before proceeding. Present a concrete plan.
DO NOT START IMPLEMENTING UNTIL I APPROVE THE PLAN.

### Intent
Implement `/pricing` with Free / Pro / Enterprise tiers using server-side Stripe pricing data.

### Constraints
- Fetch prices server-side.
- Use existing UI component patterns.
- Run `lsp_diagnostics` on changed files.
- Run `npm run build` before calling the task complete.
```

---

## Step 3: route work by job type

Do not keep UI, billing logic, and external docs in one mixed stream.

Route them like this:
- UI layout and card styling → `visual-engineering`
- billing logic and webhook handling → logic-focused agent such as `ultrabrain`
- Stripe API reference lookup → `librarian`
- repo pattern search → `explore`

If one prompt is trying to do all four, split it.

---

## Step 4: verify before you accept output

For this kind of app, use a simple verification order:

1. run `lsp_diagnostics` on changed files
2. run `npm run build`
3. review risky server logic separately

Use a review contract for the risky part, for example the Stripe webhook:

```markdown
Please review `app/api/webhooks/stripe/route.ts`.

Check:
- Stripe signature verification
- immutable event handling
- missing error handling
- any secret exposure
```

---

## Step 5: document external capability without leaking secrets

Use [../06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md](../06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md).

Record only:
- MCP server name
- env var names
- permission scope
- whether write actions require confirmation

Example:

```markdown
- Supabase DB MCP
  - Env var: POSTGRES_CONNECTION_STRING
  - Scope: read-only inspection
- GitHub MCP
  - Env var: GITHUB_PERSONAL_ACCESS_TOKEN
  - Scope: issue and PR reading
```

Do not put token values in the repo.

---

## Step 6: if the session goes wrong, reset at the right layer

### The agent starts coding before planning
Stop it. Go back to the kickoff contract and require the plan first.

### The agent invents commands
Go back to `AGENTS.md` and fix the facts layer.

### The task mixes UI, billing, and docs lookup
Split routing by job type.

### The output sounds fine but is unverified
Do not accept it until diagnostics and build checks pass.

---

## Use this case with these files

- [../PLUGINS-AND-OH-MY-OPENCODE.md](../PLUGINS-AND-OH-MY-OPENCODE.md)
- [../VIBE-CODING-WITH-OMO.md](../VIBE-CODING-WITH-OMO.md)
- [../09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](../09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)
