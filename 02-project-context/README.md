# Project Context

## Demo case: turn a repo audit into a system of record

A repo has docs, a few directories, and maybe a `.github/` folder, but no obvious build system and no explicit command reference. Use [`templates/PROJECT-FACTS-CHECKLIST.md`](templates/PROJECT-FACTS-CHECKLIST.md) to audit the repo, copy only verified facts into `AGENTS.md`, and keep everything else marked as `TBD`, not yet present, or future direction.

---

## Step-by-step workflow

1. **Open the checklist**
   - do not fill it from memory
2. **Inspect one category at a time**
   - core files
   - stack files
   - commands
   - conventions
3. **Require evidence for every item**
   - file exists
   - config exists
   - command is actually defined somewhere
4. **Sort each item into one of three buckets**
   - verified fact
   - `TBD` / not yet present
   - future direction
5. **Copy only verified facts into `AGENTS.md`**
6. **Keep missing things explicit**
   - use `TBD` or `Not yet present`
7. **Keep the checklist and `AGENTS.md` in sync**
