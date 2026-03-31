# Security Policy

This repository is primarily a documentation-and-templates project, but security still matters here.
In particular, examples, starter templates, local integration notes, and copied configuration patterns can create risk if they encourage unsafe handling of secrets, permissions, or external integrations.

---

## What should be reported

Please report issues such as:

- exposed secrets or tokens in tracked files
- documentation that suggests unsafe secret handling
- examples that encourage dangerous permission or integration patterns
- instructions that could cause users to publish sensitive data accidentally
- security-sensitive inaccuracies in integration or automation guidance

---

## What should not be reported here as a repository vulnerability

The following are usually documentation quality issues, not security incidents:

- broken links
- style inconsistencies
- missing examples
- planned features that do not exist yet

Those should go through the normal issue process instead.

---

## How to report responsibly

Please do **not** open a public issue for a real secret exposure or sensitive vulnerability.

At the moment, this repository does **not** publish a dedicated private security mailbox or reporting portal.
Until one exists, avoid posting sensitive details publicly and use the safest maintainer contact path available from the repository context.

Instead:

1. use the security reporting guidance in `.github/SECURITY_REPORTING.md`
2. include the affected file paths
3. describe the risk clearly and briefly
4. avoid reposting any secret value in full

If a tracked secret appears in this repository, limit disclosure first and avoid publishing the secret in a public issue.

---

## Scope reminder

This policy covers the contents of this repository.
It does not replace the official OpenCode security posture or vendor/service security policies.
For product-level behavior, also check official OpenCode docs and the relevant third-party service documentation.
