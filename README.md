# Firetiger Plugin for Claude Code

Add AI-powered observability to your application and interact with your production systems through natural language.

## Quick Start

1. **Install the plugin**
   ```bash
   claude plugin install firetiger
   ```

2. **Run setup**
   ```
   /firetiger:setup
   ```

3. **Deploy your app** - telemetry automatically flows to Firetiger

That's it! The setup skill will:
- Detect your tech stack (Next.js, Python, Go, etc.)
- Add OpenTelemetry instrumentation
- Create a monitoring agent tailored to your stack
- Show you what was configured

## After Setup

Once configured, use natural language to interact with your production systems:

- **"Query my logs for errors in the last hour"** - runs SQL against your telemetry
- **"What's causing the latency spike?"** - chat with your monitoring agent
- **"Create a known issue for this bug"** - track recurring problems
- **"Show me slow database queries"** - investigate performance issues
- **"Alert me on Slack when error rate exceeds 1%"** - configure monitoring

## Skills

### `/firetiger:setup`
Full onboarding - detects stack, adds instrumentation, creates agent.

### `/firetiger:instrument`
Just add OpenTelemetry instrumentation without creating an agent.

## MCP Tools

This plugin connects to Firetiger's MCP server, giving you access to:

| Tool | Description |
|------|-------------|
| `query` | Run SQL queries against your logs, traces, and metrics |
| `send_agent_message` | Chat with a monitoring agent about your system |
| `read_agent_messages` | Read agent session output |
| `create_agent_with_goal` | Create an agent with a natural language goal |
| `get_ingest_credentials` | Get OTLP endpoint for sending telemetry |

Plus full CRUD for agents, connections, known issues, runbooks, and triggers.

## Authentication

On first use, you'll be prompted to authenticate with Firetiger via OAuth. This is a one-time setup that authorizes Claude Code to access your Firetiger account.

## Manual Installation

```bash
git clone https://github.com/firetiger-inc/firetiger-plugin.git
claude --plugin-dir ./firetiger-plugin
```

## Supported Frameworks

The setup skill automatically detects and configures:

- **Node.js**: Next.js, Express, Fastify, Koa, NestJS
- **Python**: FastAPI, Django, Flask, Starlette
- **Go**: Standard library, Gin, Echo, Chi, Fiber
- **Rust**: Actix, Axum, Rocket

## Links

- [Firetiger](https://firetiger.com)
- [Firetiger Documentation](https://docs.firetiger.com)
- [GitHub Issues](https://github.com/firetiger-inc/firetiger-plugin/issues)
