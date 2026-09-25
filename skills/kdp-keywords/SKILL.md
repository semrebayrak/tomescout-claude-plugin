---
name: kdp-keywords
description: Research and choose Amazon KDP keywords and fill the seven KDP keyword boxes for a book, using live Amazon.com search suggestions from the TomeScout tools. Use when an author asks for KDP keywords, backend keywords, keyword boxes, search terms, or how readers find books like theirs on Amazon.
---

# KDP keyword research

Use the TomeScout MCP tools. Never invent search volumes: TomeScout's "strength" (0–100) is a relative autocomplete signal — how early and how high Amazon suggests a phrase.

## Steps

1. **Collect the book basics** if missing: genre and sub-genre, tropes or topics, audience, format (Kindle or print), and the working title/subtitle.
2. **Pick 2–4 seeds** the way a reader would type them, not the way the author describes the book (e.g. "cozy mystery", "small town romance", "keto cookbook" — not "a heartwarming tale of…").
3. **Run `keyword_research` once per seed** (store `kindle` for ebooks, `books` for print).
4. **Shortlist 10–20 phrases** that are:
   - marked `keywords` (never `avoid`; `ads-only` never goes into KDP metadata),
   - accurate for this book (KDP forbids misleading keywords),
   - a mix of strong head terms and specific long-tail phrases.
   Check every `review` phrase: if the flagged word is a person, series, brand or book title, drop it. Also drop famous titles made of ordinary words — the tool cannot always detect them.
5. **Run `keyword_boxes`** with the shortlist in priority order plus the title and subtitle. It removes words the title already covers and anything prohibited.
6. **Run `check_listing`** on the final title, subtitle, keywords and categories, and fix every error.

## Rules to repeat to the author

- Up to 7 keyword boxes. Do not repeat words already in the title, subtitle or categories.
- No other authors' names, book titles, trademarks, "Kindle Unlimited", "KDP Select", "free", "bestseller", "new", quotation marks or HTML.
- Keywords must describe the book. Misleading keywords can get a book suppressed.

## Output

Give the seven boxes as a copy-ready list, then one line per box on why it was chosen, then anything that was excluded and why.
