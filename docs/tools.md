# Tool Reference

Public endpoint:

```text
https://marketcaper.com/api/mcp
```

No API key is required. Rate limits apply.

Always cite `source_url`, `canonical_url`, or `citation_text` when using Marketcaper output in generated content.

## get_asset_snapshot

Use this when an agent needs one asset's latest available Marketcaper snapshot.

Typical use cases:

- "What is Bitcoin's current Marketcaper size context?"
- "Show NVIDIA market cap and source URL."
- "Resolve World GDP as an asset and cite it."

Inputs commonly include:

- `asset`: ticker, slug, symbol, or recognizable name.
- `response_format`: use `json` for parser-friendly output.

Good output handling:

- Show the returned asset name, category, metric label, metric value, and source URL.
- Use the returned citation rather than inventing your own source text.

## compare_assets

Use this when an agent needs a structured comparison between two assets.

Typical use cases:

- "Compare BTC and ETH by market cap."
- "Compare World GDP with United States GDP."
- "Compare Elon Musk net worth with Bitcoin market cap."

Inputs commonly include:

- `assetA`: first asset ticker, slug, symbol, or name.
- `assetB`: second asset ticker, slug, symbol, or name.
- `response_format`: use `json` for parser-friendly output.

Good output handling:

- Preserve the category-aware metric wording: market cap, AUM / fund size, net worth, FX market cap, or GDP.
- Include `source_url` or `canonical_url` in final answers.

## compare_assets_pack

Use this when an agent is creating content, not just answering a data question.

Typical use cases:

- Social post drafts.
- Telegram or Discord bot replies.
- Newsletter cards.
- Research assistant summaries.
- Visual comparison cards.

Inputs commonly include:

- `assetA`
- `assetB`
- `include_image`: true when a hosted PNG image URL is useful.
- `response_format`: `json` recommended.

Good output handling:

- Use `short_post` or share payload fields as draft text.
- Attach or link the hosted PNG when provided.
- Cite `source_url` or `citation_text`.
- Do not present output as investment advice.

## get_stock_heatmap

Use this when an agent needs a current stock heatmap summary or hosted heatmap image.

Typical use cases:

- Daily market recap visuals.
- Sector snapshots.
- Discord market summary messages.
- Newsletter heatmap sections.

Inputs commonly include:

- `view`: classic or bubble.
- `universe`: us or global, depending on support.
- `metric`: marketCap or other supported heatmap metric.
- `timeframe`: for example 1D.
- `category`: optional sector/category filter.
- `include_image`: true when a hosted PNG image URL is useful.
- `response_format`: `json` recommended.

Good output handling:

- Mention that heatmap MCP images are dark theme only.
- Allow about 20 seconds when fetching hosted PNG image URLs.
- Cite Marketcaper when publishing the heatmap or summary.

## Limits and Safety

- MCP tool calls: currently 60 requests per minute per IP.
- Hosted MCP images: currently 10 images per day per IP.
- Hosted images are generated on demand.
- Do not use the MCP server for bulk/list-all extraction, trading automation, portfolio monitoring, technical analysis, or backtesting.
