# Commands and Prompts

## Demo case: turn a vague docs task into a real execution contract

Someone asks: “Review this project and improve the docs.” Use the matching template in [`templates/PLAN-REQUEST.md`](templates/PLAN-REQUEST.md), [`templates/REVIEW-REQUEST.md`](templates/REVIEW-REQUEST.md), [`templates/COMMIT-REQUEST.md`](templates/COMMIT-REQUEST.md), or [`templates/PR-REQUEST.md`](templates/PR-REQUEST.md) so the agent knows what to inspect, what to produce, and when to stop.

---

## Step-by-step workflow

1. **Start with the task type**
   - planning
   - review
   - commit summary
   - PR summary
2. **Choose the matching template**
3. **Fill in the real context**
   - repo area
   - goal
   - constraints
   - output shape
4. **State what should happen first**
   - analyze only
   - plan first
   - analyze and edit
5. **Write the stopping condition**
   - wait for approval
   - provide only the draft message
   - stop after the report
6. **Remove forbidden assumptions**
   - do not invent commands
   - do not invent issue numbers
   - do not assume missing tooling exists
7. **Compare the result to the contract**
   - if the output drifted, tighten the contract
