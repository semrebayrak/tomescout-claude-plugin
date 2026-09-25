---
name: kdp-launch-listing
description: Prepare a complete Amazon KDP listing for launch — title and subtitle, description with KDP-allowed HTML, keyword boxes, price, and a starter Amazon Ads keyword list — and check it against KDP's guidelines with the TomeScout tools. Use when an author is about to publish or relaunch a book on Amazon KDP, or asks to review their Amazon book page.
---

# KDP launch listing

Work through these in order, using the TomeScout MCP tools. Show the author each draft before moving on.

## 1. Keywords first
Follow the `kdp-keywords` skill to find the phrases readers type. Reuse its shortlist below.

## 2. Title and subtitle
- The title is the title on the cover — nothing else.
- The subtitle may carry 1–2 of the strongest *accurate* phrases, written as a readable line, not a list.
- Title + subtitle must be under 200 characters. No "bestselling", "free", other authors, other books or trademarks.

## 3. Description (≤ 4,000 characters including HTML)
- Allowed tags only: `<p> <br> <b> <em> <i> <u> <h4> <h5> <h6> <ol> <ul> <li>`. No `<h1>`–`<h3>`.
- Hook in the first two lines (that is what shows above "Read more").
- No reviews, quotes or testimonials, no review requests, no prices or "on sale", no links, emails or phone numbers, no emojis, no keyword lists.

## 4. Check everything
Run `check_listing` with title, subtitle, description, the seven keywords and the three categories. Fix every error and re-run until it passes.

## 5. Price
Run `royalty_calculator`:
- eBook: compare the 70% and 35% plans at the author's price. Since 7 July 2026 the US 70% band is $2.99–$12.99. The ebook must be at least 20% cheaper than the print edition to earn 70%.
- Paperback: pass pages, ink and trim to see printing cost, royalty and the minimum list price (below $9.99 the rate drops from 60% to 50%).

## 6. Launch ads
Run `ads_keywords` with the 2–4 seeds. Author names and competing titles are fine as Amazon Ads targets even though they are banned from KDP metadata. Suggest starting with the top 30 in exact and phrase match.

## Tone
Be direct about trade-offs. Present every sales or royalty figure as an estimate with its caveat.
