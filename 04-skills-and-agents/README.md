# Skills and Agents

> **Harness role**: This module helps you route work to the right capability boundary instead of treating every task the same.

This module explains when reusable capabilities are worth creating and how to route work through OpenCode's built-in agents and skills as part of a harness.

---

## Why this matters

One of the fastest ways to make an agent system unreliable is to use the same workflow for every problem.
Some tasks need a prompt contract only. Others need a specialized agent, a reusable skill, or external reference search.

This module is about choosing the right capability boundary.

---

## 🧭 Who this module is for

Use this module if:
- you see repeated types of work in your repo
- you want more stable exploration, planning, or review behavior
- you are deciding whether a task should stay a prompt, become a skill, or be routed to an agent

---

## ⏱️ What you can finish in 15 minutes

By the end of this module, you should be able to:
1. explain the difference between a prompt contract, a skill, and an agent
2. choose a safer routing strategy for a repeated task
3. avoid over-specializing too early

---

## What this module assumes, and does not assume

This module assumes:
- you already understand repo context and prompt contracts
- you are starting to see patterns in recurring work

This module does **not** assume:
- every repeated task deserves a skill
- every hard problem needs a new agent
- community workflows replace built-in OpenCode capability

---

## 🧠 A practical routing model

Use this simple progression:

- **Prompt contract** if the task is local and the structure alone is enough
- **Skill** if the task repeats and benefits from the same specialized instructions every time
- **Agent** if the work needs a distinct reasoning role, search strategy, or quality boundary

In harness terms, this is capability routing.

---

## Demo case: should a repeated docs task become a skill?

### Situation
You keep asking the agent to audit docs for broken assumptions, missing navigation updates, and present-vs-planned drift.

### Possible routes
1. Keep writing a stronger review prompt every time
2. Turn the task into a reusable skill
3. Route parts of it to `explore` or `oracle`

### Better harness question
What is repeating?
- the wording?
- the search behavior?
- the judgment boundary?

That answer tells you whether you need a prompt, a skill, or an agent.

---

## 🛠️ Step-by-step workflow

1. **Name the repeating task**
   - for example: “doc consistency audit”
2. **Ask what repeats most**
   - instructions
   - decision rules
   - search pattern
3. **Choose the lightest useful route**
   - prompt contract first
   - skill second
   - agent when reasoning role or tooling boundary is distinct
4. **Test the route on one real task**
5. **Check if it reduces guesswork**
6. **Promote only if the benefit is real**

---

## Failure modes and recovery

### Failure mode 1: making a skill for a task that only needs a better prompt
Recovery: improve the contract first.

### Failure mode 2: using an expensive or specialized agent for trivial work
Recovery: route down, not up.

### Failure mode 3: confusing community plugin workflows with native OpenCode capabilities
Recovery: document the capability boundary clearly and keep official terms accurate.

---

## Starter assets

Use:
- [`templates/SPECIALIZATION-DECISION-CHECKLIST.md`](templates/SPECIALIZATION-DECISION-CHECKLIST.md)
- [`templates/skills/self-assessment/README.md`](templates/skills/self-assessment/README.md)

---

## Reader outcome

After this module, you should be able to decide whether a repeated task should remain a prompt contract, become a reusable skill, or be routed to a specialized agent.

---

## ⏭️ Suggested next step

Continue to [05 - Hooks and Automation](../05-hooks-and-automation/README.md) to add safe internal guardrails once routing is stable.
