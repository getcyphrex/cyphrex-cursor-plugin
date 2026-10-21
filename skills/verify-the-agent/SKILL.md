---
name: verify-the-agent
description: Don't trust the agent. Verify it. Use before secrets, money, production data, deploys, or external sends. Register the agent, check the action with Cyphrex, and read the audit log.
---

# Don't trust the agent. Verify it.

Use the Cyphrex MCP server before a risky action. Risky means secrets, money, production data, deploys, or anything sent outside the workspace.

## Tools

- `register_agent` when this agent has no Cyphrex agent id yet. Send a name, a type, and a description.
- `check_action` before the action. Send the agent id and an action object with a `type`. Stop if `allowed` is not true.
- `log_action` when an action already happened and was not sent through `check_action`. A check already writes an audit event, so do not log the same action again.
- `get_audit_log` to read what Cyphrex stored for that agent.

The key is `${CYPHREX_API_KEY}` on the MCP connection. Do not paste a key into chat, code, or tool arguments.
