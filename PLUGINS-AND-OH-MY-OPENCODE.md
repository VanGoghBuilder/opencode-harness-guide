# Plugins and oh-my-opencode

Use this file when you need to decide **what layer to use next**: built-in tools, plugins, MCP, or the oh-my-opencode community harness layer.

---

## Start here: pick the right layer

### Use built-in OpenCode tools if
- the task is local to the repo
- you only need file reads, bash, diagnostics, edits, or web fetches
- `explore`, `oracle`, or other built-in agents already cover the job

### Use a plugin if
- you want to extend OpenCode itself
- you want repeatable internal workflow behavior
- you want custom tools or hook-driven automation inside OpenCode

### Use MCP if
- OpenCode needs access to something outside the local tool surface
- you need GitHub, a database, an internal API, or another external system

### Study oh-my-opencode if
- you want a stronger community orchestration layer on top of OpenCode
- you want more structured multi-agent workflows
- you want a batteries-included harness style instead of composing everything yourself

---

## 5-minute decision flow

1. Ask: **Is the task local to this repo?**
   - yes → start with built-in tools and agents
   - no → go to step 2
2. Ask: **Do I need OpenCode to reach an external system?**
   - yes → use MCP
   - no → go to step 3
3. Ask: **Do I need stronger internal automation or custom tools?**
   - yes → use a plugin layer
   - no → stay with built-in capability
4. Ask: **Do I want a stronger orchestrated workflow than raw OpenCode gives me?**
   - yes → study oh-my-opencode
   - no → stay simpler

---

## What to do if you choose oh-my-opencode

1. Treat it as a **community extension**, not native OpenCode behavior
2. Verify the current upstream command names before copying them
3. Start from a structured kickoff, not from a free-form chat
4. Keep the planning gate: do not let it edit until the plan is clear
5. Require diagnostics and verification before you accept output

If you want the actual operating loop, go straight to [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md).

---

## What not to do

- do not use MCP for a task built-in tools already solve
- do not add a plugin just because the task feels “advanced”
- do not write community plugin commands into docs as if they are built-in OpenCode commands
- do not copy upstream examples without checking whether they still match current plugin behavior

---

## Official references to verify behavior

- Plugins: <https://opencode.ai/docs/plugins/>
- MCP servers: <https://opencode.ai/docs/mcp-servers/>
- Tools: <https://opencode.ai/docs/tools/>
- Agents: <https://opencode.ai/docs/agents/>
- Commands: <https://opencode.ai/docs/commands/>
- Rules: <https://opencode.ai/docs/rules/>

---

## Next files to open

- [VIBE-CODING-WITH-OMO.md](VIBE-CODING-WITH-OMO.md)
- [05-hooks-and-automation/README.md](05-hooks-and-automation/README.md)
- [06-integrations-and-mcp/README.md](06-integrations-and-mcp/README.md)
- [09-advanced-workflows/README.md](09-advanced-workflows/README.md)
