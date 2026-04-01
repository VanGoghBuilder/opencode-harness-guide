# AGENTS.md

## Purpose

This repository is in an early documentation-first rewrite state.
This file gives coding agents a grounded operating guide while the public documentation identity is being rewritten toward `opencode-harness-guide`.
It separates verified facts from provisional conventions.

## Verified repository facts

- Repository path: `/Users/vangogh/Documents/code/opencode-howto`
- Public documentation identity in progress: `opencode-harness-guide`
- Current state: documentation-first rewrite in progress, with the content being reframed around harness engineering
- Present root docs: `AGENTS.md`, `README.md`, `CATALOG.md`, `STYLE_GUIDE.md`, `CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `CHANGELOG.md`, `SUPPORT.md`, `.opencode/README.md`
- Present Chinese entry docs: `README.zh-CN.md`, `CATALOG.zh-CN.md`
- Present license-status file: `LICENSE`
- Present numbered modules: `01-getting-started/README.md` through `10-cli-and-terminal/README.md`
- Present Chinese module entry docs: `01-getting-started/README.zh-CN.md` through `10-cli-and-terminal/README.zh-CN.md`
- Present starter templates:
  - `01-getting-started/templates/AGENTS.md`
  - `02-project-context/templates/PROJECT-FACTS-CHECKLIST.md`
  - `03-commands-and-prompts/templates/PLAN-REQUEST.md`
  - `03-commands-and-prompts/templates/REVIEW-REQUEST.md`
  - `03-commands-and-prompts/templates/COMMIT-REQUEST.md`
  - `03-commands-and-prompts/templates/PR-REQUEST.md`
  - `04-skills-and-agents/templates/SPECIALIZATION-DECISION-CHECKLIST.md`
  - `04-skills-and-agents/templates/skills/self-assessment/SKILL.md`
  - `05-hooks-and-automation/templates/AUTOMATION-BOUNDARY-CHECKLIST.md`
  - `06-integrations-and-mcp/templates/LOCAL-INTEGRATION-NOTES.md`
  - `07-team-workflows/templates/TEAM-ONBOARDING-CHECKLIST.md`
  - `08-cross-stack-templates/templates/STACK-STARTER-READINESS-CHECKLIST.md`
  - `09-advanced-workflows/templates/ADVANCED-WORKFLOW-CHECKLIST.md`
- No package manager is currently verified in this repository
- No package manifest was found
- No lint, test, typecheck, or build config was found
- No `.cursorrules` file was found
- No `.cursor/rules/**` files were found
- No `.github/copilot-instructions.md` file was found
- Present `.github` support files: `.github/pull_request_template.md`, `.github/SECURITY_REPORTING.md`, `.github/ISSUE_TEMPLATE/bug_report.md`, `.github/ISSUE_TEMPLATE/feature_request.md`, `.github/ISSUE_TEMPLATE/documentation.md`, `.github/ISSUE_TEMPLATE/question.md`, `.github/ISSUE_TEMPLATE/config.yml`

## Project direction

The intended direction is a rewrite of the project into `opencode-harness-guide`, still inspired by `/Users/vangogh/Documents/code/claude-howto` in structure, but centered on harness engineering rather than generic how-to onboarding.
That means documentation-first structure, a clear learning path, and copy-paste-ready templates.

### Target reader

The primary audience is people using OpenCode for the first time.
Assume they need a fast on-ramp, plain explanations, and examples that work as a starting point.

### Content scope

- Follow the spirit of `claude-howto`
- Ship **docs plus reusable configuration templates**, not docs alone
- Aim long-term for broad, cross-stack coverage

Treat that as direction, not as proof that equivalent files already exist here.

## Facts first, assumptions second

Before changing anything, sort statements into two buckets:

- **Verified fact**: supported by files that exist in this repository now
- **Provisional convention**: a temporary rule used until real project structure exists

When something is not yet established, label it as `TBD`, `Provisional`, or `Not yet present`.
Do not present intended future structure as current reality.

## Pre-flight checks

Before adding files, docs, or code, check these in order:

1. What files exist right now?
2. Is there already a README, roadmap, or module structure?
3. Is a stack choice documented anywhere?
4. Is a package manager or task runner configured?
5. Are lint, format, test, typecheck, or build commands defined anywhere?
6. Are Cursor or Copilot instruction files present?
7. Is the task asking for docs, scaffolding, templates, or executable code?

If the answer is no, say so plainly and take the smallest valid next step.

## Command status

### Verified current status

No install, dev, lint, test, single-test, typecheck, or build commands are currently verified in this repository.
There is no evidence yet of `npm`, `pnpm`, `yarn`, `bun`, `make`, `just`, or custom task scripts.

### Agent rules for commands

- Do not claim a command exists unless a real file defines it
- Do not invent `package.json`, `Makefile`, CI jobs, or script names as facts
- If a task needs tooling that does not exist yet, say that explicitly and add it only if the task asks for setup

### Placeholder wording

- `Install command: TBD once a package manager is selected.`
- `Lint command: TBD once lint tooling is added.`
- `Test command: TBD once a test framework is chosen.`
- `Single test command: TBD once the test runner is chosen.`
- `Build command: TBD once the project has buildable artifacts.`

## Editing rules

- Match current repository reality, not a guessed future state
- Prefer small, additive, easy-to-review changes
- Do not create broad scaffolding unless the task asks for it
- Document new conventions near where they are introduced
- Update this file when repository facts materially change
- Do not commit or push unless explicitly asked

## Rewrite guidance

Prefer a documentation-first shape with strong navigation from the root.

### Provisional structure target

- Root `README.md` with the harness definition, audience, and fastest starting path
- `README.md` or equivalent harness build path
- `CATALOG.md`, `CATALOG.md`, or another browseable harness map
- Numbered lesson or module directories if sequential learning is chosen
- Copy-paste examples, prompts, templates, or config artifacts in obvious locations

### Rewrite priorities

1. Clarity for first-time OpenCode users
2. Discoverability from the repository root
3. Copy-paste usability
4. Consistent terminology
5. Small, reviewable content units
6. Framework-agnostic guidance where possible

### Rewrite anti-patterns

- Large walls of text with no navigation path
- Deep nesting that hides the main learning flow
- Framework-specific claims before a stack is chosen
- Examples that cannot be copied or adapted easily
- Advanced jargon before beginner framing

## Documentation expectations

Near-term work is likely documentation-heavy, so docs should answer these quickly:

1. What is this repository for?
2. Who is it for?
3. Where should a new reader start?
4. What can they finish in 15 minutes?
5. What modules exist, and in what order should they read them?
6. Which files are reference material versus hands-on exercises?
7. Which templates are safe to copy directly?

### Preferred doc qualities

- Strong opening context
- Clear beginner promise
- Short sections with useful headings
- Step-by-step flow where sequence matters
- Plain language over hype
- Internal links that reduce hunting
- Examples that can be copied without cleanup

## Writing standards

- Write for a capable beginner who wants fast clarity
- Lead with purpose, then steps, then examples
- Keep paragraphs short
- Use bullets and tables when they improve scanning
- Define terms before using shorthand
- Explain why something matters, not just what it is
- Mark placeholders and future intent clearly

See `STYLE_GUIDE.md` for the more explicit root writing contract used by this repository.

## Code style guidance for future contributions

No code style is verified yet.
Until a real stack exists, treat the following as provisional defaults only.

### Naming

- Prefer descriptive names over clever ones
- Keep user-facing terms consistent across docs and examples
- Prefer kebab-case for doc and asset filenames unless a tool requires otherwise

### Imports and module boundaries

- Prefer explicit imports over magic or hidden side effects
- Keep public entry points obvious
- Avoid deep relative import chains when a simpler structure is available

### Formatting

- Follow repository tooling once it exists
- Until then, keep formatting simple, consistent, and easy to diff

### Types and error handling

- Prefer explicit public types if a typed language is adopted
- Keep inferred local types when they are obvious
- Avoid `any`-style escape hatches unless clearly justified
- Fail with messages that help the next contributor act
- Do not swallow errors in examples without explanation

## Testing and validation

### Verified facts today

No test framework, single-test command, or build command is currently present.

### Provisional expectations

- Do not claim test coverage that does not exist
- If you add executable code, add the smallest sensible verification path
- If you add docs-only changes, check links, filenames, headings, and internal consistency
- When tooling is introduced, document lint, test, single-test, typecheck, and build commands in the README and update this file

## Cursor and Copilot rules status

No Cursor or Copilot instruction files were present when this file was written.
If `.cursorrules`, `.cursor/rules/**`, or `.github/copilot-instructions.md` are added later, treat them as repository-specific instructions and reconcile this file with them.

## When to update this file

Update `AGENTS.md` when the rewrite structure expands materially, a package manager is chosen, commands are added, local agent rules are introduced, or a real style guide replaces these defaults.

## Default stance for agents

Start small.
State what is verified.
Mark unknowns as TBD.
Prefer documentation structure over speculative scaffolding.
Make future contributions easy to read, easy to navigate, and easy to revise.
