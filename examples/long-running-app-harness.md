# Long-Running App Harness Case

Use this case when the task is too large for one short agent session, and you need the harness to keep the work coherent across planning, execution, and verification.

This case is grounded in the same core ideas Anthropic describes for long-running application development: separate planning from building, separate building from judging, keep work in bounded chunks, and verify against real system behavior instead of trusting self-praise.

---

## Step 1: create 3 explicit roles

Do not let one agent do everything.
Split the work into 3 roles:

- **Planner**: turns a short prompt into a usable product spec or task breakdown
- **Builder**: implements one bounded chunk at a time
- **Evaluator**: checks whether the chunk actually works

In OpenCode terms, you do not need to invent a giant custom system first. You can start with:
- `plan` as the planning role
- `build` or a general execution flow as the implementation role
- a separate review / QA pass as the evaluator role

If you want reusable roles, copy from:
- [../.opencode/agents/harness-planner.md](../.opencode/agents/harness-planner.md)
- [../.opencode/agents/repo-facts-checker.md](../.opencode/agents/repo-facts-checker.md)
- [../.opencode/agents/doc-link-checker.md](../.opencode/agents/doc-link-checker.md)

---

## Step 2: write a bounded spec before building

Do not start from a one-line request and let the builder improvise for hours.
Write a bounded spec or plan first.

Use one of these:
- [../03-commands-and-prompts/templates/PLAN-REQUEST.md](../03-commands-and-prompts/templates/PLAN-REQUEST.md)
- [../.opencode/commands/start-harness-task.md](../.opencode/commands/start-harness-task.md)

A good long-running spec should include:
- what the app or feature must do
- what files or areas are likely involved
- what is explicitly out of scope for this run
- what the evaluator will check before the chunk is accepted

Keep the spec high-level enough to avoid locking in the wrong implementation too early.

---

## Step 3: break the work into chunks

Do not ask the builder to finish the whole product in one pass.
Split the work into chunks that can be checked independently.

Example chunk order for a long-running app:
1. app shell and routing
2. data model and storage layer
3. one core workflow end-to-end
4. auth / permissions
5. external integrations
6. polish and edge-case fixes

Each chunk should end with one question:
**Can the evaluator tell whether this chunk is done?**

If the answer is no, the chunk is still too vague.

---

## Step 4: create a chunk contract before building

Before each chunk, write a short contract.
That contract should say:
- what will be built in this chunk
- what will not be built in this chunk
- what the evaluator will test

Minimal example:

```md
Chunk: user can create and save a project

In scope:
- create project form
- persistence to local database
- project list updates after save

Out of scope:
- sharing projects
- project deletion
- permissions model

The evaluator will check:
- form submits successfully
- saved project appears in the list
- stored data survives a reload
```

This is the simplest way to stop long-running work from drifting.

---

## Step 5: verify against real behavior, not just code shape

This is the most important rule.
Do not accept “the code looks done” as proof.

For each chunk, the evaluator should check real behavior, for example:
- browser flow works
- API returns the expected result
- stored state is actually present
- required files and routes exist
- diagnostics are clean

If your project has a browser or UI, the evaluator should act more like a QA tester than a code reviewer.

If your project has data state, verify the state, not just the form.

---

## Step 6: reset or hand off when the session gets muddy

Long-running work drifts when the session accumulates too much context or too many unfinished threads.
When that happens, do not keep pushing the same session blindly.

Instead:
1. write down current state in a short artifact
2. write the next chunk clearly
3. carry forward only the facts the next session needs

The handoff note should include:
- what is already complete
- what failed or needs rework
- what the next chunk is
- what the next evaluator must verify

This keeps the harness coherent even if the work spans many sessions.

---

## Step 7: remove harness complexity that is no longer needed

Do not keep extra harness machinery forever just because it once helped.
If the current model can handle a step without that extra scaffold, remove it.

Good rule:
- add scaffolding when it clearly improves results
- remove scaffolding when it stops being load-bearing

This keeps the harness useful instead of ceremonial.

---

## Minimal long-running app flow you can copy

1. Start with [../.opencode/commands/start-harness-task.md](../.opencode/commands/start-harness-task.md)
2. Ask the planner for a chunked plan
3. Approve only the first chunk
4. Let the builder implement only that chunk
5. Run evaluator checks on real behavior
6. Write a short handoff note for the next chunk
7. Repeat until the app is done

---

## Use this case with these files

- [../README.md](../README.md)
- [../09-advanced-workflows/README.md](../09-advanced-workflows/README.md)
- [../03-commands-and-prompts/templates/PLAN-REQUEST.md](../03-commands-and-prompts/templates/PLAN-REQUEST.md)
- [../.opencode/commands/start-harness-task.md](../.opencode/commands/start-harness-task.md)
- [../.opencode/agents/harness-planner.md](../.opencode/agents/harness-planner.md)
