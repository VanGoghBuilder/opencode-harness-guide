# Documentation Style Guide

Use this file when you are writing or rewriting docs in this repo.

---

## Write like this

When you create a user-facing doc, prefer this order:
1. tell the reader what to do first
2. point to the exact file, template, or command
3. say what to verify next
4. keep unsupported things marked as `TBD`

If a paragraph only explains an idea but does not help the user act, cut it or move it lower.

---

## Use these words consistently

- **Verified fact** = supported by a real file in the repo now
- **TBD** = intentionally unresolved because the repo does not prove it yet
- **Not yet present** = the repo does not contain it now
- **Starter template** = safe to copy, but still needs local editing

Do not blur these.

---

## Before you claim a command exists

Check which file proves it.
If no real file proves it, write `TBD` instead.

---

## Before you add a new root-facing file

Update these if needed:
- `README.md`
- `CATALOG.md`

If the file changes the bilingual entry path, update the Chinese pair too.

---

## Before you merge a doc change

Check:
- are the links real?
- did you avoid inventing commands?
- did you keep present facts separate from future plans?
- if the doc is user-facing, does it tell the reader what to do next?
