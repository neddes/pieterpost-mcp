# PieterPost MCP

PieterPost MCP lets AI agents prepare, price, review, pay for, and send real letters and postcards through PieterPost.

## Server

- MCP server URL: `https://pieterpost.com/mcp/`
- Human docs: `https://pieterpost.com/api/docs/mcp`
- Markdown docs: `https://pieterpost.com/api/docs/mcp.md`
- OAuth issuer: `https://pieterpost.com/mcp/oauth`

## What It Does

PieterPost gives MCP clients a safe postal outbox. Agents can draft letters and postcards, quote prices, create review links, create hosted payment links, upload assets, use Mailbook contacts, and check order status.

For normal use, agents should create a PieterPost review or payment link. PieterPost sends the mail only after the user reviews and pays.

## Client Configuration

Use this server URL in MCP clients that support remote Streamable HTTP servers:

```text
https://pieterpost.com/mcp/
```

Example MCP client snippet:

```json
{
  "type": "mcp",
  "name": "PieterPost",
  "server_url": "https://pieterpost.com/mcp/"
}
```

## Docs

- [Setup](docs/setup.md)
- [OAuth and permissions](docs/oauth.md)
- [Tools](docs/tools.md)
- [Safe sending flow](docs/safe-sending.md)

## Contact

For questions, contact `pieter@pieterpost.com`.
