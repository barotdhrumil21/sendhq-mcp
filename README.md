# SendHQ MCP server

Send and receive email from your verified domains; manage domains, templates and deliverability.

Official remote [Model Context Protocol](https://modelcontextprotocol.io) server for [SendHQ](https://sendhq.cc). Works in Claude, ChatGPT, Grok, Cursor, Claude Code and any MCP client that supports remote servers. Sign-in uses OAuth with your SendHQ account, so there is no API key to paste.

```
https://mcp.sendhq.cc/mcp
```

## About

Send and receive email from your verified domains, manage templates and domains, and check deliverability from Claude.

## Tools

59 tools covering sending (send_email, send_batch, drafts, templates), receiving (inboxes, threads, labels, attachments), domains (add, verify, DNS provider and Domain Connect links), and deliverability (events, suppressions, sender reputation, stats). Tools that send real email or delete data are marked so your assistant asks first.

## Connect

### Claude
Settings → Connectors → **Add custom connector**. Name it SendHQ and paste `https://mcp.sendhq.cc/mcp`, then click Connect and sign in.

Or install it from the [Claude directory](https://claude.ai/directory/sendhq).

### ChatGPT
Settings → Security and login → turn on **Developer mode**. Then go to chatgpt.com/plugins, click **Create MCP app**, enter `https://mcp.sendhq.cc/mcp` and sign in.

### Grok
Go to [grok.com/connectors](https://grok.com/connectors) → **New Connector** → **Custom**, paste `https://mcp.sendhq.cc/mcp` and sign in.

### Claude Code
```bash
claude mcp add --transport http sendhq https://mcp.sendhq.cc/mcp
```

### Cursor
Add to `~/.cursor/mcp.json`:
```json
{
  "mcpServers": {
    "sendhq": { "url": "https://mcp.sendhq.cc/mcp" }
  }
}
```

### VS Code, Windsurf and other clients
Add a remote (streamable HTTP) MCP server with the URL `https://mcp.sendhq.cc/mcp`. The client opens a browser window to sign in.

## Things to ask

- "What's in my SendHQ inbox?"
- "Send a test email from support@ my domain saying the order shipped."
- "Why did the invoice email bounce?"
- "Show my deliverability stats for this week."

## Links

- Website: https://sendhq.cc
- Connector docs: https://sendhq.cc/docs/mcp
- MCP Registry: `cc.sendhq/sendhq`

This repository holds the public connector listing only. The server is hosted by SendHQ; you need a SendHQ account to use it.
