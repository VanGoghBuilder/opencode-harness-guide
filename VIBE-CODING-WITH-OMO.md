# Vibe Coding with oh-my-opencode

"Vibe coding" means writing software primarily through natural language intent, letting agents handle syntax, exploration, and execution.
But vibe coding without guardrails quickly turns into chaos. 

**oh-my-opencode** acts as an **engineering harness** for OpenCode. It provides the missing structure: parallel exploration, explicit planning gates, specialized agent routing, and verification loops.

This is a step-by-step guide to using OpenCode + oh-my-opencode as your daily engineering harness.

---

## 🛠️ The 5-Step Vibe Coding Workflow

When you have oh-my-opencode installed, do not just start chatting and asking for code changes. Follow this structured loop:

### Step 1: Ground the context
Before you type a single prompt, ensure your repository has a basic `AGENTS.md`. OpenCode needs to know your rules, and oh-my-opencode's subagents will inherit them.
- *Action*: Ensure `AGENTS.md` is present and accurate.

### Step 2: The Kickoff (Intent)
Instead of asking OpenCode to "fix the button," you use an oh-my-opencode entrypoint to kick off a structured workflow. 
- *Action*: Use a structured kickoff prompt (see [`09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md`](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)).
- *Command*: Depending on your community plugin version, you might trigger this via `/start-work`, `ulw`, or just by explicitly asking the orchestrator to "enter analysis mode."

### Step 3: The Exploration & Planning Gate
The orchestrator will **not** start coding immediately. It will fire parallel `explore` and `librarian` background agents to read your codebase and check external docs.
- *Your job*: Sit back and let the background tasks finish. 
- *The Gate*: The orchestrator (or a `plan` subagent) will present a breakdown of the files to touch and the approach. **Review this plan.** If the design is flawed, correct the orchestrator now before any code is written.

### Step 4: Parallel Execution
Once the plan is approved, the orchestrator routes tasks to specialized agents (e.g., `visual-engineering` for UI, `ultrabrain` for hard logic). 
- *Your job*: Watch the task completions roll in. Do not micro-manage line-by-line syntax. You are the reviewer; the subagents are the typists.

### Step 5: Verification
oh-my-opencode emphasizes zero-error tolerance. The orchestrator will run `lsp_diagnostics` and compile checks.
- *Your job*: If a subagent fails, the orchestrator will automatically loop back to fix it. Only accept the work when diagnostics are clean and tests (if you have them) pass.

---

## 🚫 Vibe Coding Anti-Patterns

If you are using oh-my-opencode, stop doing these:

- **Shotgun Debugging**: Do not paste an error and say "fix this." Say: *"Fire the explore agent to find the root cause of this error in the auth module, then consult the oracle agent before proposing a fix."*
- **Micromanaging syntax**: Do not tell the agent *how* to write a regex. Tell the agent *what* the regex must catch, and let the `ultrabrain` subagent figure it out.
- **Skipping the plan**: Never let the orchestrator start modifying 5 files without showing you the file list and intent first.
- **Duplicating agent work**: If the orchestrator fires a background agent to search the codebase, do not start manually reading files in the same chat. Let the system work.

---

## 🚀 Where to go next

- Copy the kickoff template: [09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md](09-advanced-workflows/templates/OMO-VIBE-CODING-KICKOFF.md)
- Understand the technical boundary between plugins and MCP: [PLUGINS-AND-OH-MY-OPENCODE.md](PLUGINS-AND-OH-MY-OPENCODE.md)
