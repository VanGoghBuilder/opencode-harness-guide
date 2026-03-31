# OpenCode Documentation Style Guide

Use this guide when writing or editing documentation in this repository.
Its job is to keep the docs beginner-friendly, honest, and internally consistent.

---

## Audience

Write for people using OpenCode for the first time.
Assume they want a fast on-ramp, plain language, and examples they can adapt without guessing.

---

## Tone

- plain
- factual
- calm
- beginner-friendly
- honest about what is missing

Avoid hype, vague claims, and unnecessary jargon.

---

## Core terminology

Use these terms consistently:

- **Verified fact**: something supported by real files in the repository now
- **TBD**: something intentionally left unresolved until real files or decisions exist
- **Not yet present**: something the repo does not contain today
- **Starter template**: a copyable beginning point that still needs local adaptation

Do not mix these casually. The distinction between present and planned is one of the repo’s core promises.

---

## Recommended document structure

For root docs and module READMEs, prefer this shape where it fits:

1. purpose
2. who it is for
3. what you can finish in 15 minutes
4. core concept or workflow
5. what it does not assume
6. suggested next step

Not every file needs every section, but this is the default pattern.

---

## Naming and headings

- keep filenames descriptive and stable
- prefer kebab-case for doc filenames when creating new docs
- keep section titles short and useful
- avoid clever heading names that hide the real topic

When possible, use the same module names in `README.md`, `LEARNING-ROADMAP.md`, `CATALOG.md`, and module titles.

---

## Rules for claims about tooling

- do not invent install, lint, test, typecheck, build, or single-test commands
- do not imply a package manager exists unless real files prove it
- do not imply a stack is chosen unless the repo documents it clearly
- do not write future plans as if they are already implemented

When in doubt, mark something `TBD` or `Not yet present`.

---

## Link rules

- prefer relative links to files that actually exist
- do not add links to planned files until those files are created
- keep root docs cross-linked so readers do not need to hunt

If you add a new root doc, update the relevant indexes and entry points.

---

## Template-writing rules

- say what the template is for
- say whether it is safe to adapt now
- say what must be replaced locally, if applicable
- keep placeholders explicit
- keep templates small unless a larger template adds real value

Starter templates should be easy to copy into a real project with minimal cleanup.

---

## Final check before merging doc changes

- Does the doc help a first-time OpenCode user faster than before?
- Are present facts and future plans clearly separated?
- Are all links real?
- Did you avoid inventing commands or tooling?
- Did you update root indexes if you added a new file?
