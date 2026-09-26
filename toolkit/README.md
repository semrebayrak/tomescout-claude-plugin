# TomeScout Toolkit — KDP listing tools for Claude

TomeScout Toolkit helps self-published authors prepare and price a book for Amazon KDP inside Claude. It adds the
TomeScout Toolkit connector (`https://tomescout.com/mcp/toolkit`) and two skills: `kdp-listing-prep` and
`kdp-niche-sizing-by-rank`.

| Tool | What it does |
| --- | --- |
| `keyword_boxes` | Packs keyword phrases into KDP's seven 50-character keyword boxes, drops words the title already covers and refuses other authors' names, trademarks and Amazon programme names. |
| `check_listing` | Checks title, subtitle, description, keywords and categories against KDP's published metadata guidelines, with the KDP help page for each issue. |
| `royalty_calculator` | eBook 70% vs 35% in 13 Amazon stores (2026 price bands, delivery cost, VAT), paperback printing cost and royalty, Kindle Unlimited earnings. |
| `bsr_to_sales` | Turns a Best Sellers Rank into a range of daily and monthly sales from two public models. |

Results render as interactive tables and cards in Claude.

## Install

**Claude (web, desktop, mobile)**: Settings → Connectors → Add custom connector → `https://tomescout.com/mcp/toolkit`.
No sign-in is needed.

**Claude Code**

```
/plugin marketplace add semrebayrak/tomescout-claude-plugin
/plugin install tomescout-toolkit@tomescout
```

## What the plugin runs, sends and fetches

- The two skills are instructions only. The plugin has no hooks, scripts or local servers and runs no code on your
  machine.
- When Claude calls a tool, it sends that call's arguments (for example candidate keyword phrases, a title and
  subtitle, a price or a Best Sellers Rank) over HTTPS to TomeScout's server at tomescout.com. The server calculates
  the answer from those arguments, KDP's published guidelines and KDP's price tables.
- The server contacts no other service, Amazon included, and keeps nothing after it responds apart from the standard
  request logs of its host, Vercel. There is no account, sign-in or API key.

Privacy policy: https://tomescout.com/privacy · Terms: https://tomescout.com/terms · Docs: https://tomescout.com/docs

## Honest numbers

Sales-from-rank and royalty figures are estimates from public models and KDP's pricing pages, shown as ranges with
their caveats.

Amazon, Kindle and KDP are trademarks of Amazon.com, Inc. or its affiliates. TomeScout is independent and not
affiliated with Amazon.

## License

MIT — see [LICENSE](LICENSE). Security issues: see [SECURITY.md](SECURITY.md).
