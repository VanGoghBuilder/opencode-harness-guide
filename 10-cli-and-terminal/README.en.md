# CLI and Terminal Usage

## Demo case: audit a command section for truthfulness

A repo has a documentation section listing install, lint, test, and build commands, but the repo may not actually contain the files needed to support those commands. Rewrite that section so every command is classified by evidence, missing ones stay explicit, and the shell boundary stays safe.

---

## Step-by-step workflow

1. **Open the command docs**
   - `AGENTS.md`
   - README command section
   - stack-specific notes if they exist
2. **List each claimed command**
   - install
   - lint
   - test
   - typecheck
   - build
3. **Ask what file proves the command exists**
   - package manifest
   - Makefile
   - CI config
   - tool config with documented script path
4. **Classify each command**
   - verified
   - not yet present
   - `TBD`
5. **Rewrite the docs accordingly**
6. **Check shell safety boundaries while you rewrite**
   - OpenCode runs commands in the current working directory
   - prefer explicit `workdir` over `cd && ...`
   - destructive commands require explicit user consent
   - interactive commands need special handling
   - do not confuse built-in behavior with plugin behavior
7. **Keep the absence explicit**
   - an honest `TBD` is better than a fake command
   - note whether a command is local-only, CI-only, or generally usable
