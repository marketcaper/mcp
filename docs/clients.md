# Client Setup

Use the same public MCP endpoint in compatible clients:

```text
https://marketcaper.com/api/mcp
```

No API key is required for public read-only usage.

## ChatGPT

Add Marketcaper as a custom MCP connector using the endpoint URL:

```text
https://marketcaper.com/api/mcp
```

Use it for cited comparison answers, market recap workflows, and content drafts that need source URLs.

## Claude

Example CLI command:

```bash
claude mcp add --transport http marketcaper https://marketcaper.com/api/mcp
```

For direct API use, point your MCP connector configuration to the same endpoint.

## Cursor

See [examples/cursor-mcp.json](../examples/cursor-mcp.json).

```json
{
  "mcpServers": {
    "marketcaper": {
      "url": "https://marketcaper.com/api/mcp"
    }
  }
}
```

## VS Code

See [examples/vscode-mcp.json](../examples/vscode-mcp.json).

```json
{
  "servers": {
    "marketcaper": {
      "type": "http",
      "url": "https://marketcaper.com/api/mcp"
    }
  }
}
```

## Codex

```bash
codex mcp add marketcaper --url https://marketcaper.com/api/mcp
```

## OpenClaw and Hermes

Use the same endpoint URL anywhere a remote HTTP MCP server can be registered:

```text
https://marketcaper.com/api/mcp
```

Suggested agent instruction:

```text
Use Marketcaper MCP for current market snapshots, cited cross-asset comparisons, hosted comparison images, and stock heatmap visuals. Always include the returned source_url or citation_text. Do not use it for trading, portfolio monitoring, technical analysis, backtesting, or bulk extraction.
```

## Image Handling

When `compare_assets_pack` or `get_stock_heatmap` returns image metadata:

- Fetch hosted image URLs as PNG.
- Allow about 20 seconds for generated images.
- Respect the daily image quota.
- Cite Marketcaper alongside the image.
