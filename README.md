<p align="center">
  <img src="assets/firetiger.svg" alt="Firetiger logo" width="220">
</p>

# Firetiger Claude Code Plugin

The official [Claude Code](https://claude.ai/code) plugin for [Firetiger](https://firetiger.com). Firetiger agents monitor, investigate, catalog issues, and apply runbooks autonomously while Claude Code helps you build and debug code.

## Repository Layout

This repository publishes a single plugin:

- `.claude-plugin/plugin.json`: plugin manifest
- `skills/`: Firetiger skills, vendored from firetiger-oss/skills (do not edit here)
- `.mcp.json`: Firetiger MCP server configuration
- `assets/firetiger.svg`: plugin logo

## What's Included

### MCP Server

Connect to Firetiger's API for querying telemetry data, managing investigations, and interacting with AI agents directly from Claude Code.

### Skills

Skills are vendored from [`firetiger-oss/skills`](https://github.com/firetiger-oss/skills) — do not edit them here.

| Skill | Description |
|-------|-------------|
| `firetiger` | Firetiger observability toolkit — setup, instrumentation, queries, investigations, deploy monitoring, and agents |
| `firetiger-create-agent` | Create or automate a monitoring agent in Firetiger |
| `firetiger-instrument` | Instrument your application with OpenTelemetry for Firetiger |
| `firetiger-investigate` | Start or read a Firetiger investigation to diagnose issues |
| `firetiger-monitor-deploy` | Monitor a PR or deployment and review what Firetiger found |
| `firetiger-query` | Query traces, logs, and metrics with SQL |
| `firetiger-setup` | Set up Firetiger for this project — detect the stack, wire telemetry, connect integrations, create a monitoring agent |

## Resources

- [Firetiger Documentation](https://docs.firetiger.com)
- [OpenTelemetry Documentation](https://opentelemetry.io/docs/)

## License

MIT
