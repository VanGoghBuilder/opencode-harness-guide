# Skills and Agents

This chapter answers 4 concrete questions:

1. When should you **just use a built-in OpenCode agent**?
2. When should you **create a custom agent file**?
3. When should you **create a custom command file**?
4. When should you **create a `SKILL.md`**?

If you only want to know what file to create, what to put in it, and how to call it, follow the sections below in order.

---

## First, separate these 4 things

### 1. Built-in agents
The main built-in agents to care about are:
- **primary agents**: `build`, `plan`
- **subagents**: `general`, `explore`

How to use them:
- switch primary agents in OpenCode with **Tab**
- manually invoke a subagent by writing `@explore` or `@general` in your message

Example:
```text
@explore find every pricing-related implementation in this repo
```

Use built-in agents when:
- you only need repo search or analysis
- you want a plan before any edits
- you want read-only exploration

If that is enough, do **not** create new files yet.

---

### 2. Custom agents
Create a custom agent when you need a **reusable role** with stable behavior.

Good reasons to create one:
- you repeatedly do the same type of work, for example `docs-review` or `security-audit`
- you want a stable role with fixed permissions and instructions
- you want to call it directly with `@name`

Create one of these files:
- project-local: `.opencode/agents/<name>.md`
- global: `~/.config/opencode/agents/<name>.md`

Minimal example: `.opencode/agents/docs-review.md`

```md
---
description: Review docs for repo-reality drift
mode: subagent
permission:
  edit: deny
  bash: deny
---
You are a documentation review agent.
Only do these things:
- check whether commands were invented
- check whether README / INDEX / CATALOG are in sync
- check whether present facts and future plans are mixed together
Do not modify files. Output only the issue list.
```

How to call it:
```text
@docs-review check whether the latest README changes invented any commands
```

If you do not want to write the file manually, the official command is:
```bash
opencode agent create
```
That interactive flow helps you generate the agent file.

---

### 3. Custom commands
Create a custom command when you need a **repeatable entrypoint in the TUI**.

Good reasons to create one:
- you keep typing the same long prompt
- you want to run `/something` directly
- you want one fixed prompt template to target the same agent every time

Create one of these files:
- project-local: `.opencode/commands/<name>.md`
- global: `~/.config/opencode/commands/<name>.md`

Minimal example: `.opencode/commands/review-docs.md`

```md
---
description: Review documentation consistency
agent: plan
---
Check the current repository docs and report only these issues:
- invented commands
- README / INDEX / CATALOG drift
- present facts mixed with future plans
Do not modify files.
```

How to call it:
```text
/review-docs
```

If you want arguments, use `$ARGUMENTS` or `$1`, `$2`, ...

Example:

```md
---
description: Review one file for documentation drift
agent: plan
---
Review $ARGUMENTS and report:
- invented commands
- mismatch with repo reality
- required navigation updates
```

Call it like this:
```text
/review-docs README.md
```

Important distinction:
- **command** = user-facing entrypoint
- **agent** = execution role
- a command can target an agent

---

### 4. Skills (`SKILL.md`)
Create a skill when you need a **reusable method** that agents can load on demand.

Good reasons to create one:
- the reusable thing is a method, checklist, or procedure
- more than one agent may need the same method
- you want the agent to load instructions only when needed

Official file locations:
- project-local: `.opencode/skills/<name>/SKILL.md`
- global: `~/.config/opencode/skills/<name>/SKILL.md`

Minimal example: `.opencode/skills/doc-audit/SKILL.md`

```md
---
name: doc-audit
description: Audit documentation against repo reality
---
## When to use
Use this when checking whether README, INDEX, CATALOG, and AGENTS stay aligned.

## Steps
1. Check for invented commands
2. Check for mixed present facts and future plans
3. Check whether root navigation is still in sync
4. Output issues only; do not edit files unless explicitly asked
```

Official rules to remember:
- `name` must match the directory name
- `name` must be lowercase letters, numbers, and single `-`
- `SKILL.md` must be uppercase exactly

How it gets called:
- skills are not the same as `/commands`
- skills are loaded through the native `skill` tool
- as a user, the practical phrasing is:

```text
Load the `doc-audit` skill first, then review README and INDEX for drift.
```

Internal call shape:
```text
skill({ name: "doc-audit" })
```

---

## Which one should you choose right now?

Follow this order:

### I only need this once
Create nothing.
Just use:
- `plan` / `build`
- `@explore` / `@general`

### I keep repeating the same user-facing prompt
Create:
- `.opencode/commands/<name>.md`

### I need a stable reusable role
Create:
- `.opencode/agents/<name>.md`

### I need a reusable method that agents can load when needed
Create:
- `.opencode/skills/<name>/SKILL.md`

---

## The safest beginner order

If this is your first pass, do it in this order:

1. **Do not start with a skill**
2. Start with one command:
   - `.opencode/commands/review-docs.md`
3. Use it 3 to 5 times
4. If you discover the repeated thing is the role, create:
   - `.opencode/agents/docs-review.md`
5. If you discover the repeated thing is the method, create:
   - `.opencode/skills/doc-audit/SKILL.md`

This is the safest order because it delays complexity until repetition is real.

---

## Minimal practical exercise

### Goal
Add one reusable “documentation review” entrypoint to your project.

### Step 1: create a command file
Create:
- `.opencode/commands/review-docs.md`

Put this in it:

```md
---
description: Review documentation consistency
agent: plan
---
Check the current repository docs and report only these issues:
- invented commands
- README / INDEX / CATALOG drift
- present facts mixed with future plans
Do not modify files.
```

### Step 2: call it in OpenCode
```text
/review-docs
```

### Step 3: if you also need deeper repo search
Add this in the chat:
```text
@explore find every file related to README navigation
```

### Step 4: if this role becomes stable
Create:
- `.opencode/agents/docs-review.md`

### Step 5: if the stable thing is really the method
Create:
- `.opencode/skills/doc-audit/SKILL.md`

---

## Official docs to verify behavior

- Agents: <https://opencode.ai/docs/agents/>
- Commands: <https://opencode.ai/docs/commands/>
- Agent Skills: <https://opencode.ai/docs/skills/>
- Tools: <https://opencode.ai/docs/tools/>

---

## Files in this repo you can copy from

- [templates/SPECIALIZATION-DECISION-CHECKLIST.md](templates/SPECIALIZATION-DECISION-CHECKLIST.md)
- [templates/skills/self-assessment/SKILL.md](templates/skills/self-assessment/SKILL.md)
- [templates/skills/self-assessment/README.md](templates/skills/self-assessment/README.md)
