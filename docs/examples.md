# Examples

These examples are prompts and workflows for MCP-compatible clients. They intentionally do not include private keys, secrets, or application source code.

## Social comparison post

Prompt:

```text
Use Marketcaper MCP to compare BTC and ETH. Create one short social post with a source link and, if available, a hosted comparison image.
```

Recommended tool:

```text
compare_assets_pack
```

Publishing guidance:

- Use the returned short post as a draft, not as investment advice.
- Include the returned `source_url` or `citation_text`.
- If an image URL is returned, attach the PNG or link the image with the canonical pair URL.

## Telegram or Discord bot reply

Prompt:

```text
A user asks: "Is NVIDIA bigger than Apple today?" Use Marketcaper MCP to answer briefly with numbers and a citation.
```

Recommended tool:

```text
compare_assets
```

Reply shape:

```text
NVIDIA is [larger/smaller] than Apple on Marketcaper's current market cap scale. Source: [source_url]
```

## Newsletter heatmap block

Prompt:

```text
Create a short daily market recap using the US stock bubble heatmap. Include a hosted image URL and cite Marketcaper.
```

Recommended tool:

```text
get_stock_heatmap
```

Output guidance:

- Keep commentary high level.
- Mention the view, universe, metric, and timeframe.
- Include the returned image URL only if the client can fetch and display PNGs.

## Research assistant comparison

Prompt:

```text
Compare World GDP and Bitcoin using Marketcaper MCP. Explain the size relationship and cite the canonical Marketcaper page.
```

Recommended tool:

```text
compare_assets
```

Output guidance:

- Preserve category wording: GDP vs market cap.
- Avoid pretending GDP is a company market cap.
- Cite the returned source URL.

## What-if price card

Prompt:

```text
Create a cited comparison pack for XRP at Bitcoin size. Include a hosted image if available.
```

Recommended tool:

```text
compare_assets_pack
```

Output guidance:

- Use the returned calculated price wording.
- Add a clear citation.
- Do not call the result a forecast or price target.

## Bad use cases

Do not use Marketcaper MCP for:

- Automated trading.
- Portfolio monitoring.
- Backtesting.
- Technical analysis signals.
- Bulk extraction of all assets or all pairs.
- Repackaging Marketcaper data as a competing database.
