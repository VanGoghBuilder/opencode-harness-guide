# Docs Repo Harness Case

Use this case when your project is mainly documentation and templates, not an app with a verified build system.

---

## Step 1: write the repo facts first

Before asking OpenCode to rewrite docs, create or fix `AGENTS.md` so the agent can see what is real.

At minimum, write:
- what root docs exist
- what module docs exist
- which templates exist
- which commands are still `TBD`
- which support docs exist

If the repo does not prove a command exists, do not write it as real.

---

## Step 2: pick one doc target, not the whole repo

Do not start with “rewrite everything.”
Pick one target:
- root README
- one module README
- one example file
- one support doc

Good first chunk:
- rewrite `README.md` to become the single main entry point
- or clean up one module so a beginner can follow it step by step

---

## Step 3: start with a plan, not edits

Use one of these:
- [../03-commands-and-prompts/templates/PLAN-REQUEST.md](../03-commands-and-prompts/templates/PLAN-REQUEST.md)
- [../.opencode/commands/start-harness-task.md](../.opencode/commands/start-harness-task.md)

Ask for:
- which files will change
- what the new structure will be
- what links must stay valid
- what should be removed instead of rewritten

Do not approve implementation until that plan is clear.

---

## Step 4: use the right review path for docs work

If the task is documentation-heavy, do not use a generic review only.
Use these together:
- [../.opencode/commands/review-docs.md](../.opencode/commands/review-docs.md)
- [../.opencode/commands/review-readme.md](../.opencode/commands/review-readme.md)
- [../.opencode/commands/review-module.md](../.opencode/commands/review-module.md)
- [../.opencode/agents/docs-review.md](../.opencode/agents/docs-review.md)
- [../.opencode/agents/doc-link-checker.md](../.opencode/agents/doc-link-checker.md)
- [../.opencode/agents/repo-facts-checker.md](../.opencode/agents/repo-facts-checker.md)

Use them like this:
1. review wording and scope
2. review links and navigation
3. review whether facts still match real files

---

## Step 5: change root docs in this order

If the task touches root docs, use this order:
1. `README.md`
2. `README.zh-CN.md`
3. `CATALOG.md`
4. `CATALOG.zh-CN.md`
5. support docs only if the change affects reporting, contribution, or governance

This prevents root navigation drift.

---

## Step 6: keep the repo honest

For a docs repo, the most common failures are not code bugs. They are trust bugs.

Check these every time:
- invented commands
- links to deleted files
- English and Chinese entry docs drifting apart
- future plans written like present facts
- templates claiming more than the repo can support

---

## Step 7: validate before you stop

Before you call the task done:
1. run a full markdown link check
2. re-open the changed files and read them as a new contributor
3. check that deleted or merged files are no longer referenced
4. if the change affected root structure, verify `README*` and `CATALOG*` still make sense together

---

## Minimal example flow

If your task is “make the repo easier to start from,” do this:
1. update `AGENTS.md` facts first
2. rewrite `README.md` into the main entry point
3. move overflow inventory into `CATALOG.md`
4. remove redundant root intro docs
5. run review-docs
6. run link validation

---

## Use this case with these files

- [../README.md](../README.md)
- [../CATALOG.md](../CATALOG.md)
- [../AGENTS.md](../AGENTS.md)
- [../.opencode/README.md](../.opencode/README.md)
