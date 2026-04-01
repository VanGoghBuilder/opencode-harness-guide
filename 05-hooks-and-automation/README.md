# Hooks and Automation

## Demo case: classify this repo's repeated checks

This repository is docs-first. It does not have a verified package manager or test suite, but it does have many repeated documentation integrity checks. Use [`templates/AUTOMATION-BOUNDARY-CHECKLIST.md`](templates/AUTOMATION-BOUNDARY-CHECKLIST.md) to decide which checks should be automated now and which ones should stay manual.

---

## Step-by-step workflow

1. **List repeated repo tasks**
2. **Sort them into three buckets**
   - automate now
   - keep manual
   - candidate only
3. **Automate only checks with evidence and clear outcomes**
   - markdown link validation
   - root navigation drift checks
   - secret exposure checks
   - checks that unsupported commands stay marked `TBD`
4. **Keep subjective or unsupported work manual**
   - broad quality judgments
   - subjective content review
   - auto-merge behavior
   - any flow that assumes unverified tooling
5. **Write the official boundary clearly**
   - document plugins as the extension layer
   - document hooks as automation points inside that layer
6. **Put the boundary where future agents can read it**
   - keep the docs honest about what exists and what does not
