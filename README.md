# mm-inventory-reports

Public, link-shareable HTML reports on **market-maker inventory events on
HYPE** (Hyperliquid perpetuals), covering 2025-03-27 to 2026-06-30 UTC.

Start at the hub, which lists every page:
<https://hype-mm-inventory.vercel.app/> (also served at <https://xinxin-m.github.io/mm-inventory-reports/>)

Reports (short pages, each a five-minute read; dates are when the results were produced)
- **[One-sided taker surges](exp8-one-sided-surges.html)** (results 2026-09-10 to 09-22) - the 922 surges, which MMs take the inventory, and what goes with the price coming back.
- **[What a surge does to the book](exp8-surge-book-cost.html)** (results 2026-09-21 to 09-22) - spread, depth, taker cost, what moves the best quote, and where MMs place quotes.
- **[Who counts as an active MM](exp8-active-mm.html)** (results 2026-09-21 to 09-22) - the fill rule, the order-rate rule and the quiet MM-labelled days.
- **[The clause-(d) wallets, one by one](exp8-clause-d-wallets.html)** (results 2026-09-23 to 09-24) - the 306 wallets the MM label admits only through clause (d): market makers or algorithmic traders, which bots they are, and what remains to decide.
- **[MM loss episodes (z_NET)](exp8-mm-loss-episodes.html)** (results 2026-09-17 to 09-22) - which MMs lose money around a taker-imbalance event.

Where the work stands
- **[Storyline](storyline.html)** (2026-09-18) - the flow chart of how an MM inventory shock propagates, then the 2026-09-15 taker-surge chart.
- **[Plan: wrapping up the one-sided surges](plan-surge-wrapup.html)** (plan 2026-09-23, status 2026-09-24) - the order of work for the wrap-up page along the flow chart, with the active-MM and absorber tests.
- **[Change log](changelog.html)** - what each day added, every line linked to its section; kept by the site builder in `code/site_changelog.json`.

Result dump (a closed toggle in the menu)
- The full pages behind the short reports: [one-sided surges](exp8-one-sided-surges-record.html), [the book](exp8-surge-book-cost-record.html), [active MM](exp8-active-mm-record.html).

Earlier work (a closed toggle in the menu)
- [Taker imbalance, z_NET](exp8-inventory-shock-09-08.html) (obsolete), [Unwinders](exp8-unwinders.html), [Event studies](exp8-event-studies.html), [Exp10 tick level](exp10-tick-level-09-10.html), [Spot quotes](exp8-spot-quote-12-17.html), and [Exp8 - 10 roster MM](exp8-report.html) (2026-09-04, section D4 on [its own page](exp8-unwind-activity.html)).

Every page carries the same side menu and a back arrow at the top.

The review-status page (frozen on 2026-09-17) and the 2026-09-04 briefing still build at their old addresses but are no longer listed.

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
