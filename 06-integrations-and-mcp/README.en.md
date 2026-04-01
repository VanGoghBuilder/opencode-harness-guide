# Integrations and MCP

## Demo case: document a safe GitHub integration without leaking secrets

Your team wants OpenCode to inspect pull requests and issue metadata through an MCP server without ever committing a real token. Use [`templates/LOCAL-INTEGRATION-NOTES.md`](templates/LOCAL-INTEGRATION-NOTES.md) to document only the setup shape and safety boundary so teammates can configure the integration without exposing credentials or over-privileging the server.

---

## Step-by-step workflow

1. **Name the external system**
   - for example: GitHub
2. **Decide whether MCP is actually needed**
   - use built-in tools if they already solve the job
   - use plugins for stronger internal extension behavior
   - use MCP for systems outside the local tool surface
3. **Record only the setup envelope**
   - server name
   - env var names
   - required scopes or permissions
4. **Document the safety boundary**
   - read-only or write-capable
   - whether destructive actions need confirmation
5. **Keep secrets out of the repo**
   - never commit secret values
   - use environment variables or local config
   - prefer least privilege
6. **Share the note, not the credential**
