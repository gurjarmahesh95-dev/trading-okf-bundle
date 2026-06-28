---
type: trading-rules
title: Entry Rules — What Must Be True Before Buying
description: Complete checklist that must be satisfied before entering any position. Covers BVM check, Darvas confirmation, volume, grade, and order type.
tags: [entry, checklist, darvas, BVM, volume, limit-orders]
timestamp: 2026-06-28T00:00:00Z
---

# Entry Rules

## Pre-Entry Checklist (All Must Pass)

| # | Check | Pass Condition |
|---|-------|----------------|
| 1 | **BVM Green** | Brahma = Bull, Sector = Leading/Neutral, Stock = Strong | 
| 2 | **EOD Darvas close confirmed** | Stock closed above Darvas ceiling at EOD — not intraday |
| 3 | **Volume** | Entry day volume ≥ 150% of VWMA(50) |
| 4 | **Grade** | A+ or A for direct entry; B = wait for confirmation |
| 5 | **SL defined** | Stop loss placed before order; must be within 8–12% of entry |
| 6 | **R:R ≥ 2:1** | T1 target must be at least 2× the risk (prefer 3:1+) |
| 7 | **Order type** | On-stop limit order only. Market orders on open are banned. |
| 8 | **Position size** | `(Account × 1%) ÷ (Entry − Stop) = shares`. Never exceed this. |

## Entry Timing
- Enter 4–5% above the Darvas ceiling (breakout confirmation zone)
- Do not chase if price has already moved >8% above ceiling
- Preferred entry: second or third day after breakout on a minor pullback to breakout level, with volume holding up

## Pyramid Add Rule
- Add more shares at +8–10% above initial entry if volume is still confirming
- Never pyramid into a losing position

## Grade Reference

| Grade | Setup Quality | Action |
|-------|---------------|--------|
| A+ | Double Engine — strong technical + fundamental | Enter immediately |
| A | Strong momentum, good fundamentals | Enter |
| B | Developing — not all conditions met | Wait for EOD confirmation |
| C | Watchlist | No entry; monitor only |
| D/F | Weak or speculative | Avoid |

## Hard Ban: Market Orders on Open
Never enter using a market order at open. Opening prints are manipulated. Always use on-stop limit orders that trigger only when the ceiling is hit with volume.

> **Source of rule:** AEQUS (Jun 2026) — entered on opening spike before EOD Darvas confirmation. Loss taken. Rule: always wait for EOD close. Always use limit orders.

## Related
- [BVM Framework](/frameworks/bvm.md)
- [Darvas Box](/frameworks/darvas-box.md)
- [King Candle](/frameworks/king-candle.md)
- [MTF Criteria](/frameworks/mtf-criteria.md)
- [Exit Rules](/rules/exit-rules.md)
- [Core Rule Violations](/rules/violations.md)
