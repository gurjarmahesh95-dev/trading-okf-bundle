---
type: trading-framework
title: Darvas Box Methodology
description: Box consolidation breakout system adapted for Indian NSE/BSE markets. Only valid on EOD close — never intraday.
tags: [darvas, breakout, consolidation, EOD, volume]
timestamp: 2026-06-28T00:00:00Z
---

# Darvas Box Methodology

## Core Concept
A Darvas Box forms when price consolidates in a tight range (ceiling + floor) after a prior advance. A breakout above the ceiling on volume confirms the next leg up.

## Box Formation Rules
1. **Ceiling**: Highest high of the consolidation range — set after price fails to make a new high for at least 3 consecutive sessions
2. **Floor**: Lowest low of the same consolidation — must hold for the box to remain valid
3. **Duration scoring:**
   - < 3 months = poor base
   - 3–6 months = fair
   - 6–18 months = good
   - 18 months–3 years = great
   - 3 years+ = potentially explosive

## Breakout Confirmation Rules

**HARD RULE: Darvas breakout is ONLY confirmed on an EOD (End of Day) close above the ceiling. Intraday breaks do not count.**

| Condition | Required? |
|-----------|-----------|
| EOD close above ceiling | ✅ Mandatory |
| Volume ≥ 150% of VWMA(50) on breakout day | ✅ Mandatory (Mahesh Rule) |
| King Candle on breakout or prior session | ✅ Strongly preferred |
| BVM Green | ✅ Mandatory |

## Entry
- Entry 4–5% above the ceiling (breakout confirmation zone)
- Never chase if price has already moved >8% above ceiling
- Pyramid add: add more shares at +8–10% above entry if volume confirms

## Stop Loss
- Stop = floor of the box (or 8–10% below entry, whichever is tighter)
- Never widen stop after entry

## IPO Base Variant
- For recently listed stocks (< 2 years), the IPO issue price area acts as a natural floor
- IPO base breakout = stock consolidating near IPO price after listing + eventual EOD close above the listing high with volume

## Core Violation to Never Repeat
> **[AEQUS — Jun 2026]** Entered on an intraday spike before EOD confirmation. Stock opened high, Darvas ceiling not confirmed on close. Loss taken.
> **RULE: Always wait for EOD close. Set on-stop limit orders, never market orders on open.**

## Related
- [BVM Framework](/frameworks/bvm.md)
- [King Candle](/frameworks/king-candle.md)
- [Entry Rules](/rules/entry-rules.md)
- [Core Rule Violations](/rules/violations.md)
