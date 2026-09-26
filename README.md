# TomeScout — Amazon KDP research for Claude

TomeScout gives Claude (and any MCP client) live Amazon book-market data for self-published authors:

| Tool | What it does |
| --- | --- |
| `keyword_research` | What shoppers type into Amazon.com's search box (Kindle Store or Books) around a seed, ranked by autocomplete strength and marked safe for KDP keyword boxes, needs review, Amazon Ads only (author/title names) or avoid (prohibited/trademarked). |
| `keyword_boxes` | Packs phrases into KDP's seven keyword boxes, drops title words and anything prohibited. |
| `ads_keywords` | Up to 300 Amazon Ads keyword targets from 1–5 seeds. |
| `check_listing` | Title, subtitle, description, keywords and categories against KDP's published guidelines, with the KDP help page for each issue. |
| `royalty_calculator` | eBook 70%/35% in 13 Amazon stores (2026 price bands, delivery cost, VAT), paperback printing cost and royalty, Kindle Unlimited earnings. |
| `bsr_to_sales` | Best Sellers Rank → a range of daily and monthly sales from two public models. |

Results render as interactive tables and cards (MCP Apps) in Claude and ChatGPT.

This plugin adds the TomeScout connector plus three skills: `kdp-keywords`, `kdp-launch-listing` and `kdp-niche-sizing`.

## Install

**Claude Code**

```
/plugin marketplace add semrebayrak/tomescout-claude-plugin
/plugin install tomescout@tomescout
```

**Claude (web, desktop, mobile)** — Settings → Connectors → Add custom connector → `https://tomescout.com/mcp`. No sign-in needed.

**Any MCP client** — remote Streamable HTTP server at `https://tomescout.com/mcp`.

Docs: https://tomescout.com/docs

### TomeScout Toolkit (second plugin in this marketplace)

[`toolkit/`](toolkit) holds `tomescout-toolkit`: the four calculation tools (`keyword_boxes`, `check_listing`,
`royalty_calculator`, `bsr_to_sales`) from `https://tomescout.com/mcp/toolkit`, which never contacts Amazon or any
other site, plus two skills. Install it with `/plugin install tomescout-toolkit@tomescout`.

## What the connector can see

TomeScout only receives the arguments Claude sends to its tools (seed phrases, candidate keywords, the metadata you ask it to check). It does not read your conversation, files or memory, and it has no accounts. Seed phrases are sent to Amazon's public search-suggestion service. Privacy policy: https://tomescout.com/privacy

## Honest data

- Keyword data is Amazon.com only for now (US Kindle Store and Books).
- Amazon publishes no search volumes for books; "strength" is a relative ranking signal, labelled as such.
- Sales-from-rank and royalty figures are estimates from public models and KDP's pricing pages.

Amazon, Kindle and KDP are trademarks of Amazon.com, Inc. or its affiliates. TomeScout is independent and not affiliated with Amazon.

## License

MIT — see [LICENSE](LICENSE). Security issues: see [SECURITY.md](SECURITY.md).
