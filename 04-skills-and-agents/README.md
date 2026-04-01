# Skills and Agents

## Demo case: should a repeated docs task become a skill?

You keep asking the agent to audit docs for broken assumptions, missing navigation updates, and present-vs-planned drift. Use [`templates/SPECIALIZATION-DECISION-CHECKLIST.md`](templates/SPECIALIZATION-DECISION-CHECKLIST.md) to decide whether this should stay a prompt, become a reusable skill, or route part of the work to a specialized agent.

---

## Step-by-step workflow

1. **Name the repeating task**
   - for example: `doc consistency audit`
2. **Identify what repeats most**
   - instructions
   - decision rules
   - search pattern
   - review boundary
3. **Choose the lightest useful route**
   - prompt first
   - skill second
   - agent when the role or tooling boundary is distinct
4. **Test that route on one real task**
5. **Check whether it reduced guesswork**
6. **Promote complexity only when the benefit is real**
