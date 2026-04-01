# Vibe Coding with oh-my-opencode

Use this file when you want to run a task through a stronger engineering harness instead of free-form chat.

---

## The 5-step loop

### 1. Ground the repo first
Before you ask for code changes:
- make sure `AGENTS.md` exists
- make sure repo facts are current
- make sure missing commands are still marked `TBD`

If the repo map is wrong, the whole session will drift.

### 2. Start with a kickoff, not a vague request
Use [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md).

Your first message should force:
- parallel exploration
- a plan before implementation
- explicit constraints
- a stop condition

### 3. Wait for the planning gate
Do **not** let the agent start editing immediately.
First require:
- files to change
- the approach
- edge cases
- what it will verify afterward

If the plan is wrong, fix it here, not after the code lands.

### 4. Let the work route to the right capability
Do not keep everything in one giant chat flow.
Route by job type:
- UI → `visual-engineering`
- hard logic → `ultrabrain`
- external references → `librarian`
- repo search → `explore`

### 5. Verify before you accept anything
Require:
- `lsp_diagnostics` on changed files
- real command verification if your repo defines those commands
- review of risky logic before you call it done

If your repo has no verified build or test command, do not pretend it does.

---

## One practical example

### Task
“Add a pricing page to a Next.js SaaS app.”

### Better harness flow
1. start from [examples/nextjs-saas-harness.md](examples/nextjs-saas-harness.md)
2. use the kickoff template to force analysis mode
3. require a plan for page, data source, and verification
4. route UI to `visual-engineering`
5. route Stripe/server logic to the appropriate logic-focused agent
6. verify diagnostics and build before accepting the change

---

## If the session starts to go bad

### Symptom: the agent starts coding too early
Action: stop it and require the plan first.

### Symptom: the agent is guessing commands
Action: go back to `AGENTS.md` and the facts checklist.

### Symptom: one chat is trying to do everything
Action: split routing by capability.

### Symptom: the result “sounds fine” but is unverified
Action: require diagnostics or other real checks before accepting it.

---

## Use these files together

- [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md)
- [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)
- [examples/nextjs-saas-harness.md](examples/nextjs-saas-harness.md)
