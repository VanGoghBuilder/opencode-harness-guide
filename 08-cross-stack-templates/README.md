# Cross-Stack Templates

## Demo case: decide whether a Next.js starter harness is actually ready

You want to create a `Next.js + OpenCode harness starter`, but the repo you are looking at has no verified `package.json`, no lint script, and no build command. Use [`templates/STACK-STARTER-READINESS-CHECKLIST.md`](templates/STACK-STARTER-READINESS-CHECKLIST.md) to publish only the portable, verified harness layer and move unsupported stack claims out of the active path.

---

## Step-by-step workflow

1. **List the universal harness pieces**
   - `AGENTS.md`
   - facts checklist
   - planning and review contracts
2. **List the stack-specific claims you want to make**
3. **Require file evidence for each stack claim**
4. **Keep only the verified pieces**
5. **Move the rest to `TBD` or future work**
6. **Publish the universal layer now**
