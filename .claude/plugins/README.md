# Claude Code plugins

This folder is a local plugin marketplace (`kommunalwahl-plugins`). It holds
copies of these plugins from
[anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official):

| Plugin | Provides |
| --- | --- |
| `commit-commands` | `/commit`, `/commit-push-pr`, `/clean_gone` |
| `claude-code-setup` | `claude-automation-recommender` skill |
| `frontend-design` | `frontend-design` skill |

`.claude/settings.json` registers this folder and enables every plugin in it.
Claude Code offers to install them when you trust the project.

## Add a plugin

1. Copy the plugin's folder (the one containing `.claude-plugin/plugin.json`)
   into this folder.
2. Add an entry for it to `.claude-plugin/marketplace.json` with
   `"source": "./<plugin-name>"`.
3. Add `"<plugin-name>@kommunalwahl-plugins": true` to `enabledPlugins` in
   `.claude/settings.json`.

## Update a plugin

These are fixed copies and don't update automatically. To update one, replace
its folder with the current version from the upstream repository.
