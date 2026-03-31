# Plan Request

Use this as an **execution contract** when you want the agent to explore first and plan before changing anything.

Use this prompt when you want OpenCode to inspect a repository, identify unknowns, and propose the smallest useful plan.

---

Please inspect this repository before proposing changes.

In your response, cover:

1. what is already verified by real files
2. what is still unclear or `TBD`
3. the smallest useful implementation plan
4. which files are likely to change
5. what should be verified after the change

Constraints:

- do not invent commands or missing tooling
- keep future direction separate from present reality
- prefer a small plan over broad scaffolding
