# SocialDataX 敏感词检测 MCP

LobeHub 用户请使用 [LobeHub setup / 接入说明](LOBEHUB.md)，包含专属官网入口、认证和来源配置。

Hosted MCP for checking text for potential platform review risks and querying SocialDataX points balance. A result is a screening aid, not a guarantee of platform acceptance.

- Website and API Key access: https://socialdatax.com/ai?from=github
- Endpoint: https://mcp.socialdatax.com/sensitive-check/mcp
- Transport: Streamable HTTP
- Authentication: Authorization: Bearer <SOCIALDATAX_API_KEY>
- Capability version: 0.1.0
- Tools: check_sensitive_text, socialdatax_get_points_balance

The text provided to the tool is transmitted to the hosted service. Avoid including unnecessary personal or confidential information. Use your own SocialDataX API Key; do not put real keys into public files.

```json
{
  "mcpServers": {
    "socialdatax-sensitive-check": {
      "type": "streamable_http",
      "url": "https://mcp.socialdatax.com/sensitive-check/mcp",
      "headers": {"Authorization": "Bearer <SOCIALDATAX_API_KEY>"}
    }
  }
}
```

This repository contains public connection documentation and metadata only; the service implementation is privately hosted.

## Gemini CLI extension

Install this service from its public GitHub repository:

```sh
gemini extensions install https://github.com/DevinChen2014/socialdatax-sensitive-check-mcp
```

When prompted, enter your own `SOCIALDATAX_API_KEY`. Get a key from [SocialDataX](https://socialdatax.com/ai?from=github); business tool calls consume SocialDataX credits. The extension connects directly to the existing hosted MCP endpoint and does not include the private service implementation.

Verify the connection with `gemini mcp list`. To change the saved key, run:

```sh
gemini extensions config socialdatax-sensitive-check
```
