# Specialization Decision Checklist

Use this checklist before turning a repeated workflow into a reusable skill or a specialized agent.

---

## Start with the repeated work

- [ ] The repeated task is described in one sentence
- [ ] The expected outcome is clear
- [ ] The task happens often enough to justify reuse

## Is a one-off prompt enough

- [ ] The task is still changing a lot
- [ ] The repo conventions are still unsettled
- [ ] A reusable prompt pattern would cover most of the need

If these are mostly true, stay with a prompt for now.

## Is a reusable prompt pattern enough

- [ ] The task has a stable input shape
- [ ] The task has a stable output shape
- [ ] The task does not need a more specialized role yet

If these are mostly true, create a reusable prompt pattern first.

## Is a skill justified

- [ ] The work belongs to a repeatable class of tasks
- [ ] The instructions should stay consistent across many uses
- [ ] The task benefits from a shared checklist or method

## Is a specialized agent justified

- [ ] The work needs a narrower role than a general prompt
- [ ] The task quality depends on consistent specialization
- [ ] The workflow is stable enough to justify stronger structure

## Too-early signals

- [ ] The task still changes every week
- [ ] Success is not yet easy to define
- [ ] The repository is still deciding its basic workflow

If these are true, do not specialize yet.

## Final recommendation

- [ ] Stay with a one-off prompt
- [ ] Create a reusable prompt pattern
- [ ] Create a reusable skill
- [ ] Create a specialized agent
