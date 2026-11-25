# upper-funnel-ai

Claude Code plugin marketplace (`upper-funnel-marketplace`) with three demo plugins.

| Plugin   | Skill          | Agent         |
|----------|----------------|---------------|
| `baui`   | `baui-hello`   | `baui-demo`   |
| `dap`    | `dap-hello`    | `dap-demo`    |
| `common` | `common-hello` | `common-demo` |

## Layout

```
.claude-plugin/marketplace.json
plugins/
  baui/    .claude-plugin/plugin.json  skills/  agents/
  dap/     .claude-plugin/plugin.json  skills/  agents/
  common/  .claude-plugin/plugin.json  skills/  agents/
```

## Usage

```
/plugin marketplace add <path-or-repo-url>
/plugin install baui@upper-funnel-marketplace
/plugin install dap@upper-funnel-marketplace
/plugin install common@upper-funnel-marketplace
```

Test the demos with `/baui:baui-hello`, `/dap:dap-hello`, `/common:common-hello`, or ask Claude to run the `*-demo` agents.
