# Plan Request

Copy this into OpenCode when you want analysis and a plan before any file changes.

```markdown
[analyze-mode]
ANALYSIS MODE. Gather context before diving deep:

CONTEXT GATHERING (parallel):
- Fire 1-3 `explore` agents to find the current implementation and related files.
- Fire 1 `librarian` agent if external docs or third-party APIs are involved.
- Use direct tools for targeted searches while the background agents run.

SYNTHESIZE findings before proceeding.
Present:
- files to modify
- approach
- edge cases
- verification plan

DO NOT START IMPLEMENTING UNTIL I APPROVE THE PLAN.

---

### Intent
[Describe the actual task]

### Constraints
- Follow `AGENTS.md`
- Do not invent commands
- Keep unknowns as `TBD`
- [Add task-specific constraints]
```

Use this when the task is bigger than a tiny local edit.
