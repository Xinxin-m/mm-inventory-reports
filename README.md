# mm-inventory-reports

Public, link-shareable HTML reports on **market-maker inventory events on
HYPE** (Hyperliquid perpetuals), covering 2025-03-27 to 2026-06-30 UTC.

Start at the hub, which lists every page:
<https://xinxin-m.github.io/mm-inventory-reports/>

- **[Exp8 - Inventory shocks, redefinition](https://xinxin-m.github.io/mm-inventory-reports/exp8-inventory-shock-09-08.html)** (2026-09-08, newest) - market taker-flow trigger, 915 events, absolute price gate, clock-time-matched controls, the whole MM population, the 148-MM profile, two tick replays with an animated book. Supersedes the v1, v2 and v3 redefinition drafts, which are archived.
- **[Exp8 - Sudden MM inventory shocks, full report](https://xinxin-m.github.io/mm-inventory-reports/exp8-report.html)** (2026-09-04) - the original wallet-inventory study; the Exp9 order-stream results are section G. Section D4 is published in full as [its own file](https://xinxin-m.github.io/mm-inventory-reports/exp8-unwind-activity.html) because of its length; it is part of this report, not a separate study.
- **[The story so far](https://xinxin-m.github.io/mm-inventory-reports/briefing.html)** (2026-09-04) - five observation threads with figures, the candidate story, six tests, order of work
- **[Review status](https://xinxin-m.github.io/mm-inventory-reports/review-status.html)** (2026-09-04) - each point of the 2026-09-02 review, its state, and a link to where the report answers it

`index.html` is a copy of the hub, so the repository root and
`overview.html` are the same page.

## What this is

Descriptive studies of how top-volume HYPE market makers change inventory
around sudden events, measured against every wallet labeled a HYPE market
maker on the event date.

The two studies use **different event definitions and must not be pooled.**
The 2026-09-04 report detects events on ten roster wallets, so its counts and
rates describe those ten. The 2026-09-08 redefinition page detects events on
market-wide taker flow and reads the whole labeled MM population against them.

Everything is a **descriptive association** - no causal claim is made.
Detector precision (92-98%) is a count of human verdicts on rendered panels,
not a model estimate. Each page carries its own limits section.

Wallet identities are not published; MMs appear only as a volume rank.

## About these files

Generated, not authored here: every page is built from the working reports by
`make_public_site.py` in the research tree. Do not edit them in this repo - the
next build overwrites them. Pages carry `noindex, nofollow` (see `robots.txt`):
public by link, kept out of search results.
