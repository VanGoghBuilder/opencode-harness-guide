# Cross-Stack Templates

> **Harness role**: This module keeps the harness portable across different stacks without inventing unverified tooling.

This module explains what stays universal across projects and when stack-specific starter kits are justified.

---

## Why this matters

A harness should be portable, but not fake-portable.
The universal parts should transfer cleanly across repos. The stack-specific parts should wait until real files and commands justify them.

---

## 🧭 Who this module is for

Use this module if:
- you work across multiple languages or frameworks
- you want to know what parts of the harness are universal
- you are tempted to write stack-specific guides too early

---

## ⏱️ What you can finish in 15 minutes

By the end of this module, you should be able to:
1. separate universal harness patterns from stack-specific details
2. audit whether a stack starter is actually ready
3. prevent fake portability in your docs

---

## What this module assumes, and does not assume

This module assumes:
- you may want to reuse this harness approach in other repos

This module does **not** assume:
- the current repo has a chosen stack
- stack-specific commands are already verified

---

## 🧠 Universal vs stack-specific harness layers

Universal harness patterns include:
- repo context
- execution contracts
- capability routing
- automation boundaries
- feedback and review habits

Stack-specific layers include:
- concrete commands
- formatter names
- build pipelines
- framework-specific structure

---

## Demo case: decide whether a Next.js starter harness is actually ready

### Situation
You want to create a “Next.js + OpenCode harness starter,” but the repo you are looking at has no verified `package.json`, no lint script, and no build command.

### Goal
Prevent yourself from writing a fake starter kit.

### Desired result
You leave the universal harness docs reusable, but keep stack-specific guidance marked as not ready.

### Micro-example
- Keep now: `AGENTS.md`, project-facts checklist, planning/review contracts
- Move to `TBD`: `npm run lint`, `npm test`, framework-specific build steps, starter-kit claims without file evidence

---

## 🛠️ Step-by-step workflow

1. **List the universal harness pieces**
   - `AGENTS.md`
   - facts checklist
   - planning and review contracts
2. **List the stack-specific claims you want to make**
3. **Demand file evidence for each stack claim**
4. **Keep only the verified pieces**
5. **Move the rest to `TBD` or future work**
6. **Publish the universal layer now, not the fake starter later**

---

## Failure modes and recovery

### Failure mode 1: copying a stack guide from another repo and assuming it applies here
Recovery: verify every command against real files.

### Failure mode 2: claiming portability when only the wording is portable
Recovery: separate reusable patterns from stack-bound details.

### Failure mode 3: delaying all documentation because stack choices are not final
Recovery: publish the universal harness layer first.

---

## Starter asset

Use:
- [`templates/STACK-STARTER-READINESS-CHECKLIST.md`](templates/STACK-STARTER-READINESS-CHECKLIST.md)

---

## Reader outcome

After this module, you should be able to decide what part of a harness can be reused immediately and what part must wait for verified stack facts.

---

## ⏭️ Suggested next step

Continue to [09 - Advanced Workflows](../09-advanced-workflows/README.md) to orchestrate more complex work once the harness layers are clear.
