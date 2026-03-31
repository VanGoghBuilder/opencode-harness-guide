# Plugins and oh-my-opencode

This guide explains where **plugins** fit in OpenCode, how they relate to **hooks**, **agents**, **tools**, and **MCP servers**, and why **oh-my-opencode** is worth understanding if you want a more opinionated, batteries-included workflow.

---

## What this file is for

Use this guide if you are asking questions like:

- what does OpenCode mean by a **plugin**?
- how is a plugin different from an **MCP server**?
- where do **hooks** fit in?
- when should I just use built-in agents and tools instead?
- what is **oh-my-opencode**, and how should I think about using it?

---

## The short version

Use this simple map:

| Capability | Best mental model | Good for |
|---|---|---|
| **Agents / subagents** | specialized reasoning roles | exploration, architecture, review, domain-specific execution |
| **Tools** | concrete actions available to the model | reading files, running bash, diagnostics, editing, web fetches |
| **Plugins** | OpenCode extensions that can hook into events and add tools | customizing workflow behavior and adding extra capability inside OpenCode |
| **Hooks** | automation points inside plugin-driven workflows | pre-action and post-action checks, guardrails, notifications |
| **MCP servers** | external tool providers via a standard protocol | GitHub, databases, third-party services, external systems |
| **CLI / TUI** | the user-facing shell and terminal entrypoints | interactive sessions, scripting, terminal-native usage |

The key beginner distinction is this:

- **plugins extend OpenCode itself**
- **MCP servers connect OpenCode to external systems**
- **hooks are one way plugins can automate behavior**

---

## What the official OpenCode docs imply

This repository uses the official OpenCode terminology as the source of truth:

- **plugins** extend OpenCode and can add custom tools or automation behavior
- **MCP servers** expose external tools through Model Context Protocol
- **agents**, **commands**, **rules**, **tools**, and **skills** are separate product concepts

Useful official references:

- <https://opencode.ai/docs/plugins/>
- <https://opencode.ai/docs/mcp-servers/>
- <https://opencode.ai/docs/tools/>
- <https://opencode.ai/docs/agents/>
- <https://opencode.ai/docs/commands/>
- <https://opencode.ai/docs/rules/>

---

## Plugins vs hooks vs MCP

### Plugins

Think of a plugin as an **extension layer for OpenCode itself**.

Use a plugin when you want to:

- add capability inside the OpenCode environment
- standardize workflow behavior across repeated tasks
- introduce custom tools or automation points
- package a stronger opinion about how work should be routed or supervised

### Hooks

Think of hooks as **automation points**, not as a separate top-level product idea.

Use hooks when you want behavior like:

- run a check before a tool executes
- run cleanup or notification after an action
- enforce a workflow guardrail automatically

### MCP servers

Think of MCP as the **external systems bridge**.

Use MCP when you need OpenCode to talk to things like:

- GitHub
- databases
- project management systems
- internal APIs or service backends

---

## When not to reach for plugins or MCP

Do **not** reach for plugins or MCP first if your problem is simply:

- a one-off task that built-in tools already solve
- a normal codebase exploration task that `explore` already handles well
- a review or architecture decision that `oracle` already handles well
- a shell task that `bash` already handles well

Start with the smallest working abstraction. Add more system only when repetition or capability boundaries justify it.

---

## Where oh-my-opencode fits

The safest way to describe **oh-my-opencode** in this repository is:

> A **community OpenCode plugin / orchestration layer** that adds stronger workflow structure, curated agents, and extra tooling around OpenCode.

It is **not** a built-in OpenCode feature.

Public OpenCode ecosystem references describe it as a community plugin with:

- background agents
- pre-built LSP / AST / MCP tools
- curated agents
- Claude Code compatibility

---

## Why people reach for oh-my-opencode

Typical reasons include:

- stronger orchestration across multiple agents
- a more batteries-included tool surface
- pre-curated workflows for planning, execution, and review
- a more structured way to dispatch work than starting from scratch each time

If your question is “How do I make OpenCode feel more like a disciplined engineering harness?”, oh-my-opencode is one of the most relevant community extensions to study.

---

## Beginner usage guidance for oh-my-opencode

Public oh-my-opencode materials are strongly workflow-oriented. The most important beginner framing is:

1. treat it as a **community extension**, not native OpenCode behavior
2. use it when you want **more orchestration and more prebuilt workflow structure**
3. verify current upstream naming and commands before copying them into your own docs

Common public usage patterns include:

- a “just do the work” entrypoint around `ultrawork` / `ulw`
- more structured planning-oriented flows such as `/start-work`

Because those are **project-specific community workflows**, this repository should describe them as useful patterns to learn from, not core OpenCode commands.

---

## Naming note

Public oh-my-opencode materials currently show a naming transition toward **oh-my-openagent** in some places, while **oh-my-opencode** is still the more recognizable public name.

For beginner-facing docs in this repository, the safest wording is:

- say **oh-my-opencode** first for recognition
- mention that upstream materials may also use **oh-my-openagent** during the transition
- avoid assuming one single label is stable forever without checking upstream docs

---

## A practical decision rule

Use this progression:

1. **Built-in OpenCode only** if the task is simple and local
2. **Agents + tools** if the task needs better discovery, reasoning, or verification
3. **Plugins / hooks** if you need repeatable extension behavior inside OpenCode
4. **MCP** if you need access to external systems
5. **oh-my-opencode** if you want a community plugin layer with stronger orchestration and curated workflow structure

---

## Where to go next

- For plugin and hook framing: [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md)
- For external system access and MCP: [06-integrations-and-mcp/README.md](06-integrations-and-mcp/README.md)
- For orchestrating larger workflows: [09-advanced-workflows/README.md](09-advanced-workflows/README.md)
- For terminal-facing boundaries: [10-cli-and-terminal/README.md](10-cli-and-terminal/README.md)

If you want the Chinese version, see [PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md](PLUGINS-AND-OH-MY-OPENCODE.zh-CN.md).
