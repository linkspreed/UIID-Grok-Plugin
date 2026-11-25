# UIID plugin for Grok Build

This plugin connects Grok Build to the hosted UIID MCP server:

- MCP endpoint: `https://uiid.linkspreed.com/mcp`
- Publisher: LINKSPREED LLC
- Website: https://uiid.linkspreed.com
- Support: https://help.linkspreed.com
- Terms: https://legal.linkspreed.com/#/terms-of-use
- Privacy: https://legal.linkspreed.com/#/privacy-policy

## Package contents

- `.mcp.json` - Streamable HTTP MCP server configuration
- `.grok-plugin/plugin.json` - Grok plugin metadata
- `skills/uiid/SKILL.md` - UIID usage guidance
- `assets/uiid-icon.png` - plugin icon

## Installation for review

1. Upload this plugin package to the UIID plugin source repository.
2. Add a catalog entry to the official xAI plugin marketplace or open a pull request with it.
3. Sign in to Grok and install the plugin through `/plugin` when it becomes available.
4. On first use, complete the UIID OAuth authorization flow.

Do not add client secrets, provisioning keys, passwords, bearer tokens, or reviewer credentials to this package.

## Submission route

The official catalog submission uses a pull request to:

https://github.com/xai-org/plugin-marketplace

For a third-party plugin, use either:

- a remote source pinned to a full 40-character commit SHA, or
- a local vendor copy under `external_plugins/uiid`.

A remote source is the recommended production route because it lets UIID maintain plugin updates independently.

Example catalog entry:

```json
{
  "name": "uiid",
  "description": "Manage sovereign digital identities, aliases, verifiable credentials, age proofs, and delegated AI-agent identities through UIID.",
  "category": "security",
  "source": {
    "source": "url",
    "url": "https://github.com/LINKSPREED/UIID-Grok-Plugin.git",
    "sha": "FULL_40_CHARACTER_COMMIT_SHA"
  },
  "homepage": "https://uiid.linkspreed.com",
  "keywords": ["uiid", "digital identity", "identity wallet", "verifiable credentials", "AI agents"],
  "domains": ["uiid.linkspreed.com"]
}
```

Before submission, verify:

- the OAuth and authorization metadata is publicly reachable;
- MCP tool descriptions and read-only/destructive annotations are accurate;
- sample prompts work against the exact deployed server version;
- publisher name, support, terms, and privacy links are correct;
- the icon and manifest are final;
- a public upstream Git repository exists and contains this plugin package;
- the pinned commit SHA is exact and lowercase;
- `python3 scripts/generate-plugin-index.py` and `python3 scripts/validate-catalog.py` pass;
- no secrets or personal data are committed.
