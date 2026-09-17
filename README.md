# mm-inventory-reports

Public, link-shareable HTML reports on **market-maker inventory events on
HYPE** (Hyperliquid perpetuals), covering 2025-03-27 to 2026-06-30 UTC.

Start at the hub, which lists every page:
<https://hype-mm-inventory.vercel.app/> (also served at <https://xinxin-m.github.io/mm-inventory-reports/>)

Reports
- **[Exp8 - Inventory shocks](exp8-inventory-shock-09-08.html)** (2026-09-08, revised 2026-09-17, newest) - market taker-flow trigger, 915 events, every actively market-making MM around all 914 events under a post-only-fill active rule, the 148-MM profile, absorbers against flagged MMs, the one-sided taker-surge family with its own population statistics, the data caveats, synthesis, limits and decisions. The file keeps its `09-08` name so the shared link stays live; an old link into a section that moved is sent on to its new page.
- **[Exp8 - Event studies](exp8-event-studies.html)** (split out 2026-09-17) - sections 6, 7, 13 and 14 of the same record: two tick replays, and episodes 39 and 47 at one minute and at tick level.
- **[Exp8 - Unwinders](exp8-unwinders.html)** (split out 2026-09-17) - sections 4.4 and 10 to 12: the 25,705 absorbers that accumulated inventory and their early or late unwind, a shocked MM's resting orders, recovery speed over the 812 population shocks, and fast against slow unwinders (section 12.5, revised 2026-09-17).
- **[Exp10 - Absorbers at tick level](exp10-tick-level-09-10.html)** (2026-09-10, revised 2026-09-16) - episodes 39 and 47 order by order.
- **[Exp8 - Spot quotes and price discovery, 2025-12-17](exp8-spot-quote-12-17.html)** (2026-09-10) - sections 36 and 37 of the Exp8 record.

Where the work stands
- **[Change log](changelog.html)** - what each day added, every line linked to its section; kept by the site builder in `code/site_changelog.json`.
- **[The taker-surge storyline](storyline.html)** (2026-09-15) - the flow chart, with the evidence behind each node.
- **[Review status](review-status.html)** (updated 2026-09-17) - the 2026-09-11, 2026-09-15 and 2026-09-17 review points, the analysis requests, the plans, the decisions waiting, and the 2026-09-02 review.

Earlier work
- **[Exp8 - Sudden MM inventory shocks, full report](exp8-report.html)** (2026-09-04) - the original wallet-inventory study; section D4 is published in full as [its own file](exp8-unwind-activity.html).
- **[The story so far](briefing.html)** (2026-09-04).

`index.html` is a copy of the hub, so the repository root and
`overview.html` are the same page.

## What this is

Descriptive studies of how top-volume HYPE market makers change inventory
around sudden events, measured against every wallet labeled a HYPE market
maker on the event date. The two studies use **different event definitions
and must not be pooled.** Everything is a **descriptive association**; no
causal claim is made. Wallet identities are not published; MMs appear only
as a volume rank.

## About these files

Generated, not authored here: every page is built from the working reports by
`make_public_site.py` in the research tree. The three Exp8 pages are one working
file, split at build time; section, table and figure numbers are those of that
file. Finding bullets are folded to their bold headline at build time; the text
is unchanged. Do not edit them in this repo - the
next build overwrites them. Pages carry `noindex, nofollow` (see `robots.txt`):
public by link, kept out of search results. Pushing `main` deploys the site to
Vercel; GitHub Pages serves the same files.
