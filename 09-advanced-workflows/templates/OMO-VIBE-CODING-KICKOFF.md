# oh-my-opencode Vibe Coding Kickoff

Use this template as your first message to OpenCode when starting a non-trivial task using the `oh-my-opencode` community plugin / orchestration harness.

## 📝 Request

[analyze-mode]
ANALYSIS MODE. Gather context before diving deep:

CONTEXT GATHERING (parallel):
- Fire 1-3 `explore` agents to map codebase patterns and current implementations related to my goal.
- Fire 1-2 `librarian` agents if any external library or API documentation needs to be consulted.
- Use direct tools (Grep, AST-grep, LSP) for targeted searches while background agents run.

SYNTHESIZE findings before proceeding. Present a concrete plan (files to modify, approach, edge cases).

DO NOT START IMPLEMENTING UNTIL I APPROVE THE PLAN.

---

### 🎯 My Goal (Intent)
[Explain what you want to achieve, e.g., "Implement a new dark mode toggle in the site header that persists across reloads and uses Tailwind CSS."]

### 📋 Constraints & Rules
- Follow the conventions already verified in `AGENTS.md`.
- Run `lsp_diagnostics` on all changed files before claiming completion. Zero errors required.
- Ensure type-safety. No `@ts-ignore` or `as any`.
- Maintain test coverage if a test suite exists.
- If this is complex logic, consult the `oracle` agent for architecture feedback before finalizing the plan.
- If this requires visual UI changes, ensure the work is delegated to the `visual-engineering` subagent.

### 📂 Initial Context Pointers
- [Optional: Mention a starting file, e.g., "Start looking in src/components/Header.tsx"]
- [Optional: Mention related issues or previous PRs]
