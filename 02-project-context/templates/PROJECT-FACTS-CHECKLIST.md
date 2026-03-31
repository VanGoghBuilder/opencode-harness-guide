# Project Facts Checklist

Use this checklist to turn the repository into a **system of record** before asking agents to make stronger claims.

Use this checklist before writing or expanding a project instruction file.
Only mark something as true if a real file, config, or documented workflow supports it.

---

## Repository basics

- [ ] Repository name is known and documented
- [ ] Repository purpose is stated in one sentence
- [ ] Target reader or user is identified
- [ ] Existing top-level files and folders are listed

## Verified tooling status

- [ ] Package manager is verified or marked `TBD`
- [ ] Build command is verified or marked `TBD`
- [ ] Lint command is verified or marked `TBD`
- [ ] Test command is verified or marked `TBD`
- [ ] Single test command is verified or marked `TBD`
- [ ] Typecheck command is verified or marked `TBD`

## Current reality vs future direction

- [ ] Verified facts are separated from planned structure
- [ ] Missing parts are labeled `Not yet present` or `TBD`
- [ ] Future goals are not written as if they already exist

## Agent safety rules

- [ ] Agents are told not to invent commands or frameworks
- [ ] Agents are told to prefer small additive changes
- [ ] Agents are told to update guidance when reality changes

## Good final check

Before reusing this checklist, ask:

1. what is actually true today
2. what is still missing
3. what will become misleading if this file is not updated later
