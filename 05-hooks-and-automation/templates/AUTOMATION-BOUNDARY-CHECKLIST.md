# Automation Boundary Checklist

Use this checklist before automating a repeated task.

## Automate now only if all are true

- [ ] the task repeats often
- [ ] the result is easy to verify
- [ ] failure is cheap and obvious
- [ ] the repo already has the files or commands this automation depends on

## Keep manual if any are true

- [ ] the task needs subjective judgment
- [ ] the task depends on commands the repo does not verify
- [ ] the task could do damage if it runs blindly
- [ ] the task hides a decision humans should still make

## Final call

- [ ] automate now
- [ ] keep manual
- [ ] wait until repo reality is clearer
