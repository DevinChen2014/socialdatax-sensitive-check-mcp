# SocialDataX 敏感词检测 MCP

LobeHub 用户请使用 [LobeHub setup / 接入说明](LOBEHUB.md)，包含专属官网入口、认证和来源配置。

Hosted MCP for checking text for potential platform review risks and querying SocialDataX points balance. A result is a screening aid, not a guarantee of platform acceptance.

- Website and API Key access: https://socialdatax.com/ai
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
