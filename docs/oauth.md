# OAuth And Permissions

PieterPost MCP uses OAuth so MCP clients can connect to a PieterPost account without sharing API keys.

## OAuth Endpoints

- Issuer: `https://pieterpost.com/mcp/oauth`
- Authorization: `https://pieterpost.com/mcp/oauth/authorize/`
- Token: `https://pieterpost.com/mcp/oauth/token/`
- Dynamic client registration: `https://pieterpost.com/mcp/oauth/register/`
- Revoke: `https://pieterpost.com/mcp/oauth/revoke/`
- Protected resource metadata: `https://pieterpost.com/.well-known/oauth-protected-resource/mcp/`
- Authorization server metadata: `https://pieterpost.com/.well-known/oauth-authorization-server/mcp/oauth/`

## Permission Model

PieterPost separates read, send, Mailbook, and API key capabilities. Clients should request only the scopes they need.

Common capabilities:

- Read PieterPost API and MCP context.
- Quote letter and postcard orders.
- Create review, compose, checkout, or payment links.
- Upload supported mail assets.
- Use saved Mailbook contacts when authorized.
- Create direct orders only for trusted workflows with explicit confirmation.

## Safety

Letters and postcards are physical-world actions. For ordinary use, prefer review links or hosted checkout links so the user can inspect the final mail before anything is printed or sent.
