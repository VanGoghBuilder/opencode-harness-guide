# Team Workflows

> **Harness role**: This module makes the harness durable for teams instead of only useful to one operator.

This module covers onboarding, shared conventions, and keeping team guidance aligned with repository reality.

---

## Why this matters

A harness that only works for one person is not really a harness. It is a personal habit stack.
Team reliability starts when repo rules stop living only in one operator's head.

---

## 🧭 Who this module is for

Use this module if:
- you are introducing OpenCode to a team
- you want to avoid every teammate inventing their own workflow
- you want new contributors to start without guessing

---

## ⏱️ What you can finish in 15 minutes

By the end of this module, you should be able to:
1. identify what belongs in the repo vs what stays local
2. audit onboarding readiness for a new contributor
3. close one documentation gap that currently depends on tribal knowledge

---

## What this module assumes, and does not assume

This module assumes:
- one or more people besides you may use the repo soon
- some workflow knowledge already exists informally

This module does **not** assume:
- the repo already has complete onboarding docs
- every local setup can be safely committed

---

## 🧠 Shared harness vs private habit

A team harness is the documented layer that survives turnover, memory loss, and tool churn.

Good shared harness artifacts live in the repo.
Private secrets and personal preferences do not.

---

## Demo case: onboard a new contributor using only repo docs

### Situation
A new contributor needs to update one module README and keep navigation honest.

### Goal
See whether they can succeed without asking a teammate for hidden rules.

### Artifacts in play
- `AGENTS.md`
- `README.md`
- `INDEX.md`
- `CATALOG.md`
- [`templates/TEAM-ONBOARDING-CHECKLIST.md`](templates/TEAM-ONBOARDING-CHECKLIST.md)

### Desired result
You discover exactly which parts of the harness are still trapped in private knowledge.

---

## 🛠️ Step-by-step workflow

1. **Pick one realistic newcomer task**
2. **Attempt it using only repo docs**
3. **Record every point where outside help was needed**
4. **Classify each missing piece**
   - missing rule
   - missing navigation
   - missing template
   - missing support doc link
5. **Patch the repo, not the memory gap**
6. **Repeat later with a different task**

---

## What belongs in the repo

- harness rules and repo facts
- shared execution contracts
- plugin and integration guidance
- team-readable onboarding notes

## What stays local

- secrets and tokens
- personal preference settings
- machine-specific private data

---

## Failure modes and recovery

### Failure mode 1: saying “just ask me if you're confused”
Recovery: write the missing rule into the repo.

### Failure mode 2: committing secrets just to make onboarding easier
Recovery: document setup shape, not secret values.

### Failure mode 3: treating one successful onboarding as proof the harness is complete
Recovery: test a different task and look for new hidden assumptions.

---

## Starter asset

Use:
- [`templates/TEAM-ONBOARDING-CHECKLIST.md`](templates/TEAM-ONBOARDING-CHECKLIST.md)

---

## Reader outcome

After this module, you should be able to identify and reduce one concrete piece of tribal knowledge in your repo.

---

## ⏭️ Suggested next step

Continue to [08 - Cross-Stack Templates](../08-cross-stack-templates/README.md) to decide what in the harness is universal and what should remain stack-specific.
