# Advanced Workflows

## Demo case: expand a thin module into a real harness playbook

A module README is too thin for a new contributor to use, and your task is to rewrite it so they can follow it without asking for hidden context. Use [`templates/ADVANCED-WORKFLOW-CHECKLIST.md`](templates/ADVANCED-WORKFLOW-CHECKLIST.md) and [`templates/OMO-VIBE-CODING-KICKOFF.md`](templates/OMO-VIBE-CODING-KICKOFF.md) to rewrite it into a usable playbook built around one real demo case and clear workflow boundaries.

---

## Step-by-step workflow

1. **Explore the current state**
   - read the module
   - read related templates
   - inspect root navigation expectations
2. **Define the rewrite goal**
   - what failure should this module prevent?
   - what should the reader be able to do afterward?
3. **Set a planning gate**
   - outline sections before rewriting
4. **Rewrite around one demo case**
   - situation
   - goal
   - artifacts
   - steps
   - failure modes
5. **Route unmet needs honestly**
   - internal extension behavior belongs with plugins
   - outside systems belong with MCP
   - stronger community orchestration belongs with oh-my-opencode
   - unclear stop conditions go back to planning
6. **Verify links, file references, and claims**
7. **Do one clarity pass**
