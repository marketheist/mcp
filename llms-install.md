# Installing the MarketHeist MCP server

MarketHeist is a **remote** MCP server. There is nothing to clone, build or install, and no API key or environment variable is needed.

Add this entry to the client's MCP settings. For Cline, that is `cline_mcp_settings.json`:

```json
{
  "mcpServers": {
    "marketheist": {
      "type": "streamableHttp",
      "url": "https://api.marketheist.io/api/mcp",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

- Transport: Streamable HTTP
- URL: `https://api.marketheist.io/api/mcp`
- Authentication: none

To check it works, call `list_indicators`. It returns the 12 built-in indicators. Then try `analyze_portfolio` with `{"template": "all-weather"}`.

All four tools (`list_indicators`, `run_backtest`, `analyze_portfolio`, `decompose_factors`) are read-only.
