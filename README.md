<p align="center">
  <img src="assets/firetiger.svg" alt="Firetiger logo" width="220">
</p>

# Firetiger Claude Code Plugin

The official [Claude Code](https://claude.ai/code) plugin for [Firetiger](https://firetiger.com). Firetiger agents monitor, investigate, catalog issues, and apply runbooks autonomously while Claude Code helps you build and debug code.

## Repository Layout

This repository publishes a single plugin:

- `.claude-plugin/plugin.json`: plugin manifest
- `commands/`: Firetiger skills exposed to Claude Code
- `.mcp.json`: Firetiger MCP server configuration
- `assets/firetiger.svg`: plugin logo

## What's Included

### MCP Server

Connect to Firetiger's API for querying telemetry data, managing investigations, and interacting with AI agents directly from Claude Code.

### Skills

| Skill | Description |
|-------|-------------|
| `firetiger:setup` | Full onboarding - detects stack, adds instrumentation, connects integrations, creates agent |
| `firetiger:instrument` | OpenTelemetry instrumentation for Node.js, Python, Go, and Rust applications |
| `firetiger:create-agent` | Create a monitoring agent with a natural language goal |
| `firetiger:monitor-deploy` | Set up deployment monitoring for a PR via GitHub integration |
| `firetiger:query` | Query traces, logs, and metrics with SQL via Firetiger MCP |
| `firetiger:investigate` | Start an investigation to diagnose issues |

## Resources

- [Firetiger Documentation](https://docs.firetiger.com)
- [OpenTelemetry Documentation](https://opentelemetry.io/docs/)

## License

MIT
