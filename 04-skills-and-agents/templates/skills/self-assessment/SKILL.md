# Self-Assessment Skill

This skill acts as an interactive quiz to help users find their OpenCode proficiency level.

## Description
Interactive quiz to evaluate OpenCode proficiency across all 10 feature areas. Generates a personalized learning path based on the user's current knowledge.

## Instructions
1. When invoked, greet the user and explain that you will ask them 5 quick questions about their OpenCode usage to determine their level.
2. Ask the questions one by one, waiting for the user's response before proceeding to the next.

### The Questions:
- Q1: "Have you ever created an `AGENTS.md` or a context file for your project to ground OpenCode?"
- Q2: "Do you use structured prompt templates (like a `PLAN-REQUEST.md`) instead of just typing instructions from scratch?"
- Q3: "Have you ever loaded a custom `SKILL.md` using the `skill` tool or used a built-in OpenCode agent like `explore` or `librarian`?"
- Q4: "Are you familiar with OpenCode's hooks and have you configured any automation boundaries?"
- Q5: "Have you successfully set up an MCP (Model Context Protocol) server to connect OpenCode to external tools (like GitHub or a database)?"

### Scoring & Recommendation:
- **0-1 Yes**: Level 1 (Beginner). Recommend starting at [Module 01: Getting Started](../../../01-getting-started/README.md).
- **2-3 Yes**: Level 2 (Intermediate). Recommend starting at [Module 04: Skills and Agents](../../../04-skills-and-agents/README.md).
- **4-5 Yes**: Level 3 (Advanced). Recommend checking out [Module 09: Advanced Workflows](../../../09-advanced-workflows/README.md) and [Module 06: Integrations and MCP](../../../06-integrations-and-mcp/README.md).

3. After all questions are answered, calculate the score, announce their Level, and provide the specific module links they should read next based on their gaps.
