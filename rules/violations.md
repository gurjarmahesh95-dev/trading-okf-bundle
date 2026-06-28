---
type: trading-rules
title: Core Rule Violations — Never Repeat These
description: Hard-coded mistakes from real trades. These are permanent prohibitions, not guidelines. Any setup resembling these patterns gets a JOURNAL WARNING.
tags: [violations, discipline, behavioral, ban, mistakes]
timestamp: 2026-06-28T00:00:00Z
---

# Core Rule Violations

These are permanent. No exceptions. Any new setup that resembles one of these gets a `⚠️ JOURNAL WARNING` in the analysis output.

---

## VIOLATION 1 — Intraday Entry Before EOD Darvas Confirmation
**Stock:** AEQUS + SHAILY (Jun 2026)
**What happened:** Entered on an intraday opening spike before the Darvas ceiling was confirmed on an EOD close. Stock reversed. Loss taken.

**Permanent ban:**
> Never enter a Darvas breakout on an intraday price. Only an EOD close above the ceiling counts. Always use on-stop limit orders that trigger only at or above the ceiling, not market orders at open.

---

## VIOLATION 2 — Market Order on Opening Spike
**Stock:** NETWEB (Jun 8, 2026)
**What happened:** Used a market order for exit after intraday drop. Filled near the day's low — 10% below the intraday high of the same day.

**Permanent ban:**
> Market orders for entries and exits are banned. All orders must be limit orders. On exits after intraday drops, place limit order 2–3% above current bid.

---

## VIOLATION 3 — Panic Exit on Minor Pullback in Stage-2 Uptrend
**Stock:** MTAR Technologies (Feb 9, 2026)
**What happened:** Exited during a 2-day, 3.5% pullback in a clean stage-2 uptrend. Stock went +167% after exit.

**Permanent ban:**
> Never exit a stage-2 uptrend stock (making higher highs + higher lows) on a pullback of <5% lasting <5 days. Only exit on EOD close below 20-day EMA or breakdown of prior swing low on volume.

---

## VIOLATION 4 — Selling at a Round Number as if it is Resistance
**Stock:** Laurus Labs (Dec 15, 2025)
**What happened:** Sold at ₹999 treating ₹1,000 as resistance. Stock went to ₹1,457 (+46%).

**Permanent ban:**
> Round numbers (₹100, ₹500, ₹1,000, ₹5,000) are support zones, not automatic sell points. Do not exit near a round number without a confirmed close below it on volume.

---

## VIOLATION 5 — Exiting on Price Discomfort When Thesis is Intact
**Stock:** Ather Energy (Dec 3, 2025)
**What happened:** Sold on a 10% pullback. EV thesis was fully intact. Stock went +55%.

**Permanent ban:**
> If the thesis invalidation trigger (defined at entry) has not fired, do not exit on price discomfort alone. A 10–15% pullback in a growth stock with intact thesis is normal volatility.

---

## How to Apply
When analyzing any new trade or exit:
1. Does this setup involve an intraday entry? → ⚠️ VIOLATION 1 WARNING
2. Is the user placing a market order? → ⚠️ VIOLATION 2 WARNING
3. Is the user exiting a stage-2 stock on a <5% pullback? → ⚠️ VIOLATION 3 / MTAR WARNING
4. Is the user selling near a round number? → ⚠️ VIOLATION 4 WARNING
5. Is the thesis still intact but user wants to exit? → ⚠️ VIOLATION 5 WARNING

## Related
- [Exit Rules](/rules/exit-rules.md)
- [Entry Rules](/rules/entry-rules.md)
- [Darvas Box](/frameworks/darvas-box.md)
