# CLAUDE.md

This repo is a Claude Code plugin marketplace (`upper-funnel-marketplace`) with three plugins: `baui`, `dap` and `common`.

## Layout

- `.claude-plugin/marketplace.json` lists the plugins. Each entry's `source` points to `./plugins/<name>`.
- `plugins/<name>/.claude-plugin/plugin.json` is the plugin manifest (name, description, version).
- `plugins/<name>/skills/<skill-name>/SKILL.md` holds skills, with `name` and `description` frontmatter.
- `plugins/<name>/agents/<agent-name>.md` holds agents, with `name`, `description` and `tools` frontmatter.

Only `plugin.json` goes inside `.claude-plugin/`. Keep `skills/` and `agents/` at the plugin root.

## Conventions

- Skill names are `<plugin>-<purpose>` (e.g. `baui-hello`). Agent names are `<plugin>-<purpose>` (e.g. `baui-demo`).
- Adding a plugin means creating `plugins/<name>/` and adding an entry to `marketplace.json`.
- Bump `version` in the plugin's `plugin.json` when its behavior changes.
- Keep `README.md` plugin table in sync with the plugins, skills and agents.
- The existing skills and agents are demos. Replace them with real content as plugins mature.

## Testing locally

```
/plugin marketplace add /Users/ogibrncrdobamndez/dev/upper-funnel-ai
/plugin install <name>@upper-funnel-marketplace
```

Then run `/<plugin>:<skill>` or ask Claude to use the plugin's agent.

## Rules

- Never commit secrets, tokens, PII or customer data. This repo is public.
- Follow the organization security policy (read-only AWS roles, no production mutations).
- Remote: `https://github.tlcinternal.com/ogibrncrdobamndez/upper-funnel-ai`, branch `main`.
