# Commands and Prompts

> **Harness role**: This module defines execution contracts so the agent works against explicit intent instead of vague chat.

This module covers reusable request patterns. It separates official OpenCode command terminology from the structured prompts you use to control work.

---

## Why this matters

A capable agent still fails if the request contract is weak.
Vague prompts force the agent to guess scope, desired output, and stopping conditions.

This module prevents that by turning natural language into a harness contract.

---

## 🧭 Who this module is for

Use this module if:
- you are tired of typing long, repetitive instructions from scratch
- you want stable planning and review behavior
- you want to define the difference between built-in commands and repo-specific workflows

---

## ⏱️ What you can finish in 15 minutes

By the end of this module, you should be able to:
1. distinguish built-in commands from prompt contracts
2. convert a vague request into a structured execution request
3. choose the right request pattern for planning, review, commit, or PR work

---

## What this module assumes, and does not assume

This module assumes:
- you have some repo context already
- you are trying to control agent behavior through wording

This module does **not** assume:
- custom slash commands exist in your repo
- the repo already has automation or plugin support
- every workflow is backed by executable tooling

---

## 🧠 Commands vs execution contracts

In OpenCode:
- **Commands** are built-in instructions such as `/skills` or `/playwright`, plus native tools
- **Prompt contracts** are the structured requests you write so the agent knows what to do, what not to do, and what a good result looks like

The harness view is simple:
- commands expose capability
- prompt contracts govern execution

---

## Demo case: turn a vague docs task into a real execution contract

### Weak request
“Review this project and improve the docs.”

### Why it fails
The agent still has to guess:
- which docs?
- improve for whom?
- should it explore first?
- should it implement or only report?
- how should it present the result?

### Stronger harness contract
Use a structure like this:
- context gathering first
- explicit goal
- file or area hints
- forbidden assumptions
- output format
- stop condition

That is exactly what the templates in this module are for.

---

## 🛠️ Step-by-step workflow

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
4. **Remove ambiguity before sending**
   - what should happen first?
   - should the agent only analyze or also change files?
5. **State stopping conditions**
   - plan first
   - wait for approval
   - provide only the draft message
6. **Compare the result to the contract**
   - if the output drifted, improve the contract, not just the next reply

---

## Worked comparison

### Vague version
“Can you help me write a PR?”

### Contract version
“Please analyze my current branch and recent commits, then draft a PR description with Summary, Motivation, Changes made, How to test, and Impact. Do not invent commands or issue numbers.”

The second version gives the agent a clear boundary and a predictable output shape.

---

## Failure modes and recovery

### Failure mode 1: mixing built-in commands and community workflows
Recovery: document built-in commands separately from community or repo-specific entrypoints.

### Failure mode 2: overloading one prompt with multiple unrelated jobs
Recovery: choose one contract and one main output per request.

### Failure mode 3: asking for implementation when you really need analysis first
Recovery: add a planning gate explicitly.

---

## Starter assets

Use:
- [`templates/PLAN-REQUEST.md`](templates/PLAN-REQUEST.md)
- [`templates/REVIEW-REQUEST.md`](templates/REVIEW-REQUEST.md)
- [`templates/COMMIT-REQUEST.md`](templates/COMMIT-REQUEST.md)
- [`templates/PR-REQUEST.md`](templates/PR-REQUEST.md)

---

## Reader outcome

After this module, you should be able to turn a vague instruction into a reusable execution contract that produces more predictable behavior.

---

## ⏭️ Suggested next step

Continue to [04 - Skills and Agents](../04-skills-and-agents/README.md) to decide when a prompt contract is enough and when the harness should route work differently.
