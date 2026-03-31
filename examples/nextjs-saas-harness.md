# Next.js SaaS Harness — OpenCode Harness Case

> A real-world example of applying the OpenCode Engineering Harness to a Next.js + Supabase + Stripe SaaS application.
> Copy this structure to your project root to ground your agents in reality.

## 1. The Map (`AGENTS.md`)

This is your minimal harness entry point. It tells the agent what is real and what rules to follow.

```markdown
# Repository Harness Context

- **Stack**: Next.js 15 (App Router), TypeScript, Supabase (Auth + DB), Stripe (Billing), Tailwind CSS
- **Architecture**: Server Components by default. Client Components only for interactivity.
- **State**: Greenfield, basic scaffolding exists, `npm run dev` works.

## Critical Harness Rules

### Database & Auth
- All queries MUST use the Supabase client with RLS enabled. Never bypass RLS.
- Migrations live in `supabase/migrations/`. Do not modify the database directly via SQL prompts.
- Use `createServerClient()` from `@supabase/ssr` in Server Components.

### Code Style & Constraints
- Immutable patterns only: use spread operator, never mutate objects directly.
- Server Components: no `'use client'` directive, no `useState`/`useEffect`.
- Prefer Zod schemas for all API route and form input validation.

### Automation Boundaries
- `npm run lint` and `npm run build` MUST pass before claiming a task is complete.
- Do NOT automate PR merging.
```

## 2. The Execution Contract (`PLAN-REQUEST.md`)

When you want the agent to build a new feature (e.g., adding a pricing page), use this contract instead of a vague prompt.

```markdown
# Harness Execution Contract

[analyze-mode]
ANALYSIS MODE. Gather context before diving deep:

CONTEXT GATHERING (parallel):
- Fire 1-3 `explore` agents to map the current Stripe billing implementation in `src/lib/stripe/`.
- Fire 1 `librarian` agent to check the latest Next.js 15 Server Action patterns if needed.

SYNTHESIZE findings before proceeding. Present a concrete plan (files to modify, components to create, API routes needed).

DO NOT START IMPLEMENTING UNTIL I APPROVE THE PLAN.

---

### 🎯 Intent
Implement the `/pricing` page displaying 3 tiers (Free, Pro, Enterprise) fetching dynamic pricing data from Stripe.

### 📋 Constraints
- Fetch prices server-side. Never trust client-side price data.
- Use Shadcn/ui components for the pricing cards.
- Ensure `lsp_diagnostics` are clean after implementation.
```

## 3. Feedback Loops & Verification

Do not accept code blindly. Run the verification loop.

1. **Diagnostics**: Ask the agent to run `lsp_diagnostics` on all modified files.
2. **Build**: Ask the agent to run `npm run build` to catch Server/Client component boundary errors.
3. **Review**: Use a review contract if the logic is complex:

```markdown
# Review Contract

Please review the newly added Stripe webhook handler in `app/api/webhooks/stripe/route.ts`.

- Does it verify the Stripe signature correctly?
- Does it handle the `checkout.session.completed` event immutably?
- Are there any exposed secrets or unhandled errors?
```

## 4. Capability Routing

Instead of doing everything in one chat, route the work:
- **UI Tweaks**: Route to the `visual-engineering` subagent to style the pricing cards with Tailwind.
- **Billing Logic**: Route to the `ultrabrain` subagent to handle the webhook parsing and database updates.
- **External Docs**: Use `librarian` to look up the exact Stripe API payload format.

## 5. Integrations & MCP (`LOCAL-INTEGRATION-NOTES.md`)

Document your external dependencies safely so the team can use the harness without leaking secrets.

```markdown
# External Capability Requirements

This project uses MCP for database inspection and GitHub issue tracking.

- **Supabase DB**: Use the Postgres MCP server.
  - Env var required: `POSTGRES_CONNECTION_STRING` (Do NOT commit this!)
  - Scope: Read-only access to verify migrations applied correctly.
- **GitHub**: Use the GitHub MCP server to read feature requests.
  - Env var required: `GITHUB_PERSONAL_ACCESS_TOKEN`
```
