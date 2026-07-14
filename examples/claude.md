# Claude Example

Add Marketcaper MCP with the Claude CLI:

```bash
claude mcp add --transport http marketcaper https://marketcaper.com/api/mcp
```

Example prompt:

```text
Use Marketcaper MCP to create a cited market comparison post for ETH vs BTC. Include the source URL and hosted image metadata if available.
```

For parser-friendly output, ask for JSON and preserve Marketcaper citation fields in the final answer.

Suggested use cases:

- Cited market comparison answers.
- Newsletter cards.
- Telegram or Discord bot replies.
- Stock heatmap recap summaries.

Not intended for trading, portfolio monitoring, technical analysis, backtesting, or bulk extraction.
