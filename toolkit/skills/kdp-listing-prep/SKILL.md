---
name: kdp-listing-prep
description: Prepare an Amazon KDP listing before publishing — title and subtitle, a description with KDP-allowed HTML, the seven keyword boxes and the price — and check it against KDP's published guidelines with the TomeScout Toolkit tools. Use when an author is about to publish or relaunch a book on Amazon KDP, asks for their seven keyword boxes, or asks to review their book's metadata.
---

# KDP listing prep

Work through these in order with the TomeScout Toolkit tools, and show the author each draft before moving on. The toolkit calculates from what it is given; it does not look anything up on Amazon.

## 1. Candidate keyword phrases
Collect or draft with the author 10–20 phrases a reader would type into Amazon's search box for this book: genre, sub-genre, tropes, setting, audience. Use the reader's words, not the blurb's, and keep every phrase accurate for the book. The author can test a phrase by typing it into Amazon's search box and reading the suggestions.

## 2. Keyword boxes
Run `keyword_boxes` with the phrases in priority order plus the title and subtitle. It packs seven 50-character boxes, removes words the title already covers and drops prohibited, trademarked and likely author or title phrases. Also drop famous titles made of ordinary words, which the tool cannot always detect.

## 3. Title and subtitle
- The title is the title on the cover and nothing else.
- The subtitle may carry one or two of the strongest accurate phrases, written as a readable line rather than a list.
- Title and subtitle together stay under 200 characters, with no "bestselling", "free", other authors, other books or trademarks.

## 4. Description (up to 4,000 characters including HTML)
- Allowed tags only: `<p> <br> <b> <em> <i> <u> <h4> <h5> <h6> <ol> <ul> <li>`.
- A hook in the first two lines, which is what shows above "Read more".
- No reviews or quotes, no review requests, no prices or "on sale", no links, emails or phone numbers, no emojis and no keyword lists.

## 5. Check everything
Run `check_listing` with the title, subtitle, description, the seven keywords and up to three categories. Fix every error and run it again until it passes.

## 6. Price
Run `royalty_calculator`:
- eBook: compare the 70% and 35% plans at the author's price. Since 7 July 2026 the US 70% band is $2.99–$12.99, and the ebook must be at least 20% cheaper than the print edition to earn 70%.
- Paperback: pass pages, ink and trim to see the printing cost, the royalty and the minimum list price (below $9.99 the rate drops from 60% to 50%).

Present every royalty figure as an estimate based on KDP's published pricing pages.
