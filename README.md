# Agrowise AI Marketplace

A plugin marketplace for **Agrowise** Claude Code and Codex plugins.

This repo hosts the marketplace manifest and (eventually) the plugin sources that power Agrowise's internal Claude Code / Codex tooling — reusable skills, agents, and workflows shared across Agrowise projects.

## Structure

- `.claude-plugin/marketplace.json` — the marketplace manifest consumed by Claude Code's plugin marketplace system.
- `plugins/` — individual plugin sources. Each plugin lives in its own subdirectory with its own `.claude-plugin/plugin.json` (or Codex equivalent).

## Adding this marketplace to Claude Code

```
/plugin marketplace add ebizuwo/agrowise-ai-marketplace
```

Then browse and install plugins with `/plugin install <plugin-name>@agrowise-ai-marketplace`.

## Adding a new plugin

1. Create a new directory under `plugins/<plugin-name>/`.
2. Add the plugin's manifest and skill/agent/command files.
3. Register the plugin in `.claude-plugin/marketplace.json`.
4. Open a PR.

## Status

Early scaffold — no plugins published yet.
