# Codex Example

Add Marketcaper MCP:

```bash
codex mcp add marketcaper --url https://marketcaper.com/api/mcp
```

Example prompt:

```text
Use Marketcaper MCP to compare BTC and NVDA. Give me a concise cited answer and include a hosted comparison image if available.
```

Suggested use:

- Use `compare_assets` for structured comparison answers.
- Use `compare_assets_pack` when drafting social posts, newsletter snippets, or bot replies.
- Use `get_stock_heatmap` for market recap visuals.
- Always cite the returned `source_url` or `citation_text`.

Avoid using Marketcaper MCP for trading automation, portfolio monitoring, backtesting, technical analysis, or bulk extraction.
