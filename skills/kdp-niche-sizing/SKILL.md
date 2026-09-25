---
name: kdp-niche-sizing
description: Estimate whether an Amazon book niche is worth writing for, using search-suggestion strength and the Best Sellers Rank of the top books the author sees on Amazon, with TomeScout's keyword research and BSR-to-sales tools. Use when an author asks if a genre, trope or topic sells, how much competing books sell, or which niche to write next.
---

# KDP niche sizing

## Demand: what readers type
Run `keyword_research` on the niche phrase. A seed strength above ~50 and many specific follow-on phrases suggest real reader demand. Few or no suggestions suggest readers do not search for it in those words — try the words readers would use.

## Supply: what the top books sell
Ask the author to search the niche on Amazon.com and read the "Best Sellers Rank" (the overall store rank, e.g. "#4,512 in Kindle Store") of 5–10 top results. Then run `bsr_to_sales` for each rank (`kindle` or `print`).

Summarise:
- the range of monthly units for the typical top-10 book (use the middle of the pack, not the #1 outlier),
- how many of the top 10 sell more than ~5 units a day,
- with the author's royalty per sale from `royalty_calculator`, the monthly royalty range a book at the median rank would earn.

## Honesty rules
- Rank-to-sales figures come from public models; always show the range, the confidence, and that Kindle ranks also reflect Kindle Unlimited borrows.
- One BSR reading can be a one-day spike. Suggest checking the same books on a few different days.
- Never promise sales. A niche with strong demand and a few weak top books is an opportunity; one dominated by big-name authors needs a sharper angle.
