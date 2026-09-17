# mm-inventory-reports

Public, link-shareable HTML reports on **market-maker inventory events on
HYPE** (Hyperliquid perpetuals), covering 2025-03-27 to 2026-06-30 UTC.

Start at the hub, which lists every page:
<https://hype-mm-inventory.vercel.app/> (also served at <https://xinxin-m.github.io/mm-inventory-reports/>)

Reports
The report pages are grouped by the event definition they read. The one Exp8 working file is published as five pages; section, table and figure numbers are those of the single record, and an old link into a section that moved is sent on to its new page.

Net taker imbalance, |z_NET| >= 3.70 on 30-minute boxes (event sets 1 and 2)
- **[Exp8 - Net-flow events](exp8-inventory-shock-09-08.html)** (2026-09-08, revised 2026-09-17) - the Summary, notation and event-set key for every definition; the shock definition, every actively market-making MM around all 914 events, the 148-MM profile, absorbers against flagged MMs, the data caveats, synthesis, limits and decisions. The file keeps its `09-08` name so the shared link stays live.
- **[Exp8 - Unwinders](exp8-unwinders.html)** (split out 2026-09-17) - sections 4.4 and 12: early and late unwinders among the 25,705 absorbers that accumulated, and how fast and slow unwinders quote.

One-sided taker surges, family F1 (event set 3)
- **[Exp8 - One-sided surges](exp8-one-sided-surges.html)** (split out 2026-09-17) - section 9: the 922 side surges against the net rule, with the section 4 statistics rerun on F1.

Wallet inventory shocks, |z| >= 6 on a wallet's own inventory (event sets 4 and 5)
- **[Exp8 - Event studies](exp8-event-studies.html)** (split out 2026-09-17) - sections 6, 7, 13 and 14: two tick replays, and episodes 39 and 47 at one minute and at tick level.
- **[Exp8 - Resting orders, recovery](exp8-resting-orders-recovery.html)** (split out 2026-09-17) - sections 10 and 11: a shocked roster MM's resting orders, and recovery speed over the 812 population shocks.
- **[Exp10 - Absorbers at tick level](exp10-tick-level-09-10.html)** (2026-09-10, revised 2026-09-16) - episodes 39 and 47 order by order.
- **[Exp8 - Spot quotes and price discovery, 2025-12-17](exp8-spot-quote-12-17.html)** (2026-09-10) - sections 36 and 37 of the Exp8 record.

Where the work stands
- **[Change log](changelog.html)** - what each day added, every line linked to its section; kept by the site builder in `code/site_changelog.json`. A slider sets how many days count as new (0 to 7, default 1, kept per browser); pages split out of already-published sections are never new.
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
