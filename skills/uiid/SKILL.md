---
name: uiid
description: >-
  Work with sovereign digital identities, cryptographic aliases, verifiable
  credentials, zero-knowledge age proofs, and delegated AI-agent identities
  through the UIID MCP server. Use when UIID, UIID Core, aliases, trust scores,
  identity verification, credentials, age proofs, or AI-agent identities are mentioned.
---

# UIID

Use the `uiid` MCP server at `https://uiid.linkspreed.com/mcp` for UIID identity operations.

## Before acting

1. Resolve identity and authorization first. Call the appropriate profile or discovery tool before changing account state.
2. Never invent identifiers, provisioning keys, aliases, credentials, or proof results. Use only values returned by the service or explicitly supplied by the user.
3. Do not request or store passwords, private keys, seed phrases, bearer tokens, or provisioning secrets in chat.
4. Present tool output accurately. Clearly report missing fields, authorization failures, validation failures, and unsupported operations.

## Safe behavior

- Treat profile, alias, credential, verification, and agent data as sensitive.
- Summarize personal information only for the user's immediate task.
- Before destructive or delegated actions, confirm the exact target and action with the user.
- For permanent deletion or permission revocation, state the scope clearly and use only an explicitly exposed tool.
- For age proofs, request only the minimum age threshold needed for the task and never infer or disclose a date of birth.
- Do not claim that an identity is verified unless the verification tool returned that result.

## Unsupported requests

Do not use UIID tools for unrelated banking, arbitrary financial transfers, credential fabrication, or permanent core-identity deletion unless a dedicated exposed tool supports that exact operation.

## Example prompts

- Show my UIID profile and trust status.
- List the aliases connected to my UIID.
- Create a new alias named Travel.
- Verify this UIID Core ID or Alias.
- Generate an age proof for minimum age 18 without revealing my date of birth.
- Show my AI agents and explain their delegated permissions.
