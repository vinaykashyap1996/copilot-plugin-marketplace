# Copilot Plugin Marketplace

One central marketplace. Each plugin (skills, agents, prompts, hooks, MCP servers) lives in its own repository; this repo only holds the catalog.

## Structure

- `.github/plugin/marketplace.json` — catalog pointing to plugin repos
- `plugins/all-skills/` — legacy local bundle

## Plugins

| Plugin | Source |
|---|---|
| `inmation-web-agent-skills` | [aspentechnology/eop-inmation-web-agent-skills](https://github.com/aspentechnology/eop-inmation-web-agent-skills) |
| `skill-summarizer` | [simple-copilot-plugins-app/plugins/skill-summarizer](https://github.com/vinaykashyap1996/simple-copilot-plugins-app/tree/master/plugins/skill-summarizer) |
| `agent-triage` | [simple-copilot-plugins-app/plugins/agent-triage](https://github.com/vinaykashyap1996/simple-copilot-plugins-app/tree/master/plugins/agent-triage) |
| `mcp-local-tools` | [simple-copilot-plugins-app/plugins/mcp-local-tools](https://github.com/vinaykashyap1996/simple-copilot-plugins-app/tree/master/plugins/mcp-local-tools) |
| `all-skills` | `./plugins/all-skills` (local) |

## Install

```sh
copilot plugin marketplace add vinaykashyap1996/copilot-plugin-marketplace
copilot plugin marketplace browse copilot-plugin-marketplace
copilot plugin install inmation-web-agent-skills@copilot-plugin-marketplace
copilot plugin install mcp-local-tools@copilot-plugin-marketplace
```

## Adding a plugin from another repo

1. Put a `plugin.json` (with `skills`, `agents`, `mcpServers`, etc.) in that repo.
2. Add an entry to `.github/plugin/marketplace.json`:

```json
{
  "name": "my-plugin",
  "source": { "source": "github", "repo": "owner/repo" }
}
```

Add `"path": "sub/folder"` if the plugin is not at the repo root.

Note: installers need read access to each plugin repo (e.g. private org repos).
