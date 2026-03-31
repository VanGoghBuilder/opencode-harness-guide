# Contributing

Thanks for helping improve `opencode-howto`.
This repository is a documentation-first rewrite for first-time OpenCode users, so the best contributions are usually the ones that make the project easier to enter, easier to trust, and easier to copy from.

Before contributing, also read [LICENSE](LICENSE). This repository is public, but it does **not yet publish a final open-source license**, so reuse and downstream expectations should not be assumed beyond what that file currently states.

---

## What good contributions look like

Good contributions usually do one or more of these:

- improve beginner clarity
- add or refine copyable starter templates
- make navigation easier from the root
- fix wording drift between root docs, modules, and templates
- keep present facts separate from future plans

---

## Before you change anything

Check these first:

1. what files already exist
2. whether the thing you want to describe is already real in the repo
3. whether the change belongs in a root doc, a module, or a starter template
4. whether you are adding facts or future direction

If a command, toolchain, or stack choice is not verified, do not write it as if it already exists.

---

## Writing and editing rules

- follow [STYLE_GUIDE.md](STYLE_GUIDE.md)
- use [AGENTS.md](AGENTS.md) for repo-grounded agent guidance
- prefer small, reviewable changes
- keep docs framework-agnostic unless the repo has real stack-specific material
- update indexes when you add a new root doc or template
- when you add or remove a root-facing learning asset, update the full navigation surface: `README.md`, `QUICK_REFERENCE.md`, `INDEX.md`, and `CATALOG.md`

---

## Suggested contribution flow

1. start from [README.md](README.md) and [INDEX.md](INDEX.md)
2. find the module or root doc you need to improve
3. make the smallest useful change
4. check links, headings, and present-vs-planned wording
5. update `CATALOG.md` or `AGENTS.md` if repository facts changed materially
6. if the change affects the beginner path or starter-template set, update `README.md`, `QUICK_REFERENCE.md`, and `INDEX.md` too

For public issues, use the repository issue templates.
For security-sensitive reports, use [SECURITY.md](SECURITY.md) and [.github/SECURITY_REPORTING.md](.github/SECURITY_REPORTING.md) instead of a normal issue.
For serious conduct issues, use [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) and [SUPPORT.md](SUPPORT.md) first and avoid posting sensitive personal details in public threads.

> Current limitation: this repository does not yet publish a dedicated private reporting channel for security or conduct issues. If a report requires private handling, do not post sensitive details publicly.

---

## Common anti-patterns

- inventing commands that no file defines
- adding stack-specific guidance before the stack exists in the repo
- expanding a small beginner doc into a giant reference wall
- leaving new files unindexed from the root
- writing future aspirations as current repository facts

---

## Pull request guidance

Keep pull requests small and easy to review.
If your change adds a new doc, include:

- why it is needed
- which existing docs it connects to
- whether it changes present facts or just adds guidance

If a change introduces a new convention, document it close to the files that will rely on it.
