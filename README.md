# Copilot Plugin Marketplace

A marketplace repository for bundling and installing Copilot plugins from a single source.

## Structure

- `.github/plugin/marketplace.json` — marketplace catalog
- `plugins/all-skills/` — bundle plugin containing multiple skills

## Install

```sh
copilot plugin marketplace add vinaykashyap1996/copilot-plugin-marketplace
copilot plugin marketplace browse copilot-plugin-marketplace
copilot plugin install all-skills@copilot-plugin-marketplace
```
