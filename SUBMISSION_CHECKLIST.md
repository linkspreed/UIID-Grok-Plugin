# UIID Grok submission checklist

## Package

- [ ] Review `.mcp.json` endpoint
- [ ] Review `.grok-plugin/plugin.json` metadata
- [ ] Review `skills/uiid/SKILL.md`
- [ ] Replace the placeholder repository URL if it differs
- [ ] Confirm LICENSE and terms are appropriate
- [ ] Confirm icon dimensions and rendering
- [ ] Run JSON validation
- [ ] Run a live MCP handshake
- [ ] Test OAuth in a clean browser session
- [ ] Test read operations
- [ ] Test authorization failures
- [ ] Test destructive or delegated operations with confirmation
- [ ] Remove secrets and private test data

## Marketplace repository

- [ ] Fork `xai-org/plugin-marketplace`
- [ ] Create an external plugin source repository
- [ ] Commit this package to the source repository
- [ ] Obtain `git rev-parse HEAD`
- [ ] Add the 40-character SHA to `.grok-plugin/marketplace.json`
- [ ] Run `python3 scripts/generate-plugin-index.py`
- [ ] Run `python3 scripts/validate-catalog.py`
- [ ] Open a pull request
- [ ] Complete code-owner review

## Reviewer evidence

- [ ] Record a real demo video or GIF
- [ ] Document tested prompts
- [ ] Link support and privacy pages
- [ ] List tested regions and limitations
- [ ] Document permissions and OAuth scopes
