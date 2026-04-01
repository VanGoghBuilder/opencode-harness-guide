# Contributing

If you want to improve this repository, use this order.

---

## Before you change anything

1. Read [README.md](README.md)
2. Read [AGENTS.md](AGENTS.md)
3. Read [LICENSE](LICENSE)
4. If the change affects public docs, also read:
   - [INDEX.md](INDEX.md)
   - [CATALOG.md](CATALOG.md)
   - [QUICK_REFERENCE.md](QUICK_REFERENCE.md)

Do not assume this repo is under a final open-source license yet. Check `LICENSE` first.

---

## If you want to add or rewrite docs

1. Verify the repo fact first
   - if a command is not defined by a real file, keep it as `TBD`
2. Edit the target file
3. Update navigation if the change affects root-facing docs:
   - `README.md`
   - `QUICK_REFERENCE.md`
   - `INDEX.md`
   - `CATALOG.md`
4. If the change affects bilingual entry docs, update the Chinese side too:
   - `README.zh-CN.md`
   - `QUICK_REFERENCE.zh-CN.md`
   - `INDEX.zh-CN.md`
   - `CATALOG.zh-CN.md`
5. Run a link check or equivalent verification

---

## If you want to add a new starter asset

Create the file in the right place:
- starter repo entry → `01-getting-started/templates/`
- facts / context → `02-project-context/templates/`
- execution contracts → `03-commands-and-prompts/templates/`
- routing / skills / agents → `04-skills-and-agents/templates/`
- automation / integration / orchestration → `05` to `09` template folders

Then update:
1. `CATALOG.md`
2. `INDEX.md`
3. `README.md` if it is a root-facing asset
4. Chinese entry docs if the asset is user-facing in the main path

---

## If you want to report a sensitive issue

Do not open a normal public issue first.
Read:
- [SECURITY.md](SECURITY.md)
- [SUPPORT.md](SUPPORT.md)
- [.github/SECURITY_REPORTING.md](.github/SECURITY_REPORTING.md)

---

## What good contributions look like here

Ship changes that make the repo:
- easier to start from
- easier to trust
- easier to copy from
- harder for agents to misread

Avoid changes that only make the repo sound smarter while making it harder to operate.
