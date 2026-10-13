# Installing Nummerschilderen.com shop advisor in Cline

This is a hosted remote MCP server. There is nothing to clone, build or install.

Add this entry to `cline_mcp_settings.json`:

```json
{
  "mcpServers": {
    "nummerschilderen": {
      "type": "streamableHttp",
      "url": "https://mcp.nummerschilderen.com/mcp",
      "disabled": false
    }
  }
}
```

Authentication: No authentication. Public, read-only endpoint.

No credentials are needed.

Check the connection by asking: "Find a paint-by-number kit with a landscape, 40x50 cm."
