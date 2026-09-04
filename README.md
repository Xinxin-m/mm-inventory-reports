# mm-inventory-reports

Public, link-shareable HTML reports on **market-maker inventory events on
HYPE** (Hyperliquid perpetuals), covering 2025-03-27 to 2026-06-30 UTC.

- **[Review status (home)](https://xinxin-m.github.io/mm-inventory-reports/)** - each point of the 2026-09-02 review, its state, and a link to where the report answers it
- **[Briefing - Exp5 and Exp8 in 15 minutes](https://xinxin-m.github.io/mm-inventory-reports/briefing.html)**
- **[Exp8 - Sudden MM inventory shocks, full report](https://xinxin-m.github.io/mm-inventory-reports/exp8-report.html)**
- **[About these pages](https://xinxin-m.github.io/mm-inventory-reports/overview.html)**

Site: <https://xinxin-m.github.io/mm-inventory-reports/>

## What this is

Two descriptive studies of how ten top-volume HYPE market makers change
inventory around sudden events, measured against every wallet labeled a HYPE
market maker on the event date.

Everything is a **descriptive association on a five-minute grid** - no causal
claim is made. Events are detected on ten wallets only, so counts and rates
describe those ten. Detector precision (92-98%) is a count of human verdicts on
rendered panels, not a model estimate. Each report carries its own limits
section.

Wallet identities are not published; desks appear only as a volume rank.

## About these files

Generated, not authored here: both pages are built from the working reports by
`make_public_site.py` in the research tree. Do not edit them in this repo - the
next build overwrites them. Pages carry `noindex, nofollow` (see `robots.txt`):
public by link, kept out of search results.
