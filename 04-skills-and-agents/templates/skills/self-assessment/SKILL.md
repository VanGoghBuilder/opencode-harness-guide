---
name: self-assessment
description: Ask a learner a few quick questions and point them to the next OpenCode harness module.
---
## When to use
Use this when someone needs a quick starting point and does not know which part of the harness guide to read first.

## Steps
1. Ask 5 short questions about their current OpenCode usage.
2. Count how many answers are effectively "yes".
3. Route them to the next module based on the score.

## Questions
- Have you created an `AGENTS.md` or another repo context file?
- Do you use structured request templates instead of ad hoc prompts?
- Have you used built-in agents such as `explore` or `general`, or loaded a real skill?
- Have you defined automation boundaries or hooks?
- Have you set up an MCP server for any external system?

## Routing
- 0 to 1 yes: start at [Module 01: Getting Started](../../../../01-getting-started/README.md)
- 2 to 3 yes: start at [Module 04: Skills and Agents](../../../README.md)
- 4 to 5 yes: continue with [Module 06: Integrations and MCP](../../../../06-integrations-and-mcp/README.md) and [Module 09: Advanced Workflows](../../../../09-advanced-workflows/README.md)

## Output rule
Keep the recommendation tied to files that actually exist in this repository.
