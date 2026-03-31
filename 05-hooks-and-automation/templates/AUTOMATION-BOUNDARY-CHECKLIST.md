# Automation Boundary Checklist

Use this checklist before you automate a check, trigger, or repeated workflow.

---

## Why automate this

- [ ] The workflow is repeated often enough to justify automation
- [ ] The automation protects something important
- [ ] The expected result is clear and checkable

## Why not automate this yet

- [ ] The workflow is still changing a lot
- [ ] The repository lacks the files or tooling needed to check it
- [ ] The automation would mostly add noise or friction

## Safety checks

- [ ] The automated step will not invent missing project facts
- [ ] The step will not assume commands that are still `TBD`
- [ ] The step is understandable to future contributors
- [ ] The failure message will help someone act on it

## Good final question

If this automation fails tomorrow, will a new contributor understand why and know what to do next?
