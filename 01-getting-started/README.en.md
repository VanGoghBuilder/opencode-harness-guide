# Getting Started

## Demo case: your first 15 minutes in a blank-ish repo

You open a repo that has a `README.md`, a few folders, and some docs, but no obvious package manifest and no command reference. Use [`templates/AGENTS.md`](templates/AGENTS.md) to create the smallest possible harness entry point so the agent stops guessing. At the end, the repo should have a starter `AGENTS.md` that says what is real, what is missing, and what the agent should not invent.

---

## Step-by-step workflow

1. **Inspect the root**
   - list the top-level files and folders
   - only inventory what exists
2. **Separate facts from assumptions**
   - write down only what real files support
   - treat anything else as unverified
3. **Mark unknowns as `TBD`**
   - use `TBD` for anything the repo does not prove yet
4. **Copy the starter `AGENTS.md`**
   - start from [`templates/AGENTS.md`](templates/AGENTS.md)
5. **Replace placeholders with real repo facts**
   - present files and folders
   - missing toolchains or commands
   - current project direction, if documented
6. **Add one safe operating rule**
   - use: `Do not invent commands that no file defines.`
7. **Re-read the file once as if you were the agent**
   - confirm it says what exists
   - confirm it says what is missing
   - confirm it blocks unsafe guesses
