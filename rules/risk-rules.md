---
type: trading-rules
title: Risk Rules — Position Sizing and Portfolio Limits
description: Hard risk management rules covering position size formula, daily loss limits, portfolio concentration, and time stops.
tags: [risk, position-sizing, portfolio, limits, bamboo]
timestamp: 2026-06-28T00:00:00Z
---

# Risk Rules

## Position Sizing Formula
```
Shares = (Account Value × 1%) ÷ (Entry Price − Stop Loss Price)
```
- Max 1% of account at risk per trade
- Never override this to "make up" for a missed entry or a losing streak

## Portfolio Limits
- **Max stocks:** 15–20 in swing portfolio (Bamboo rule: focus = edge)
- **Max new entries per week:** 3
- **Never add a 21st stock** unless one is exited first

## Daily Loss Limit
- **2% daily loss limit** — if hit, stop trading for the day
- **3 consecutive losses** → halve position size next week + mandatory journal review before next entry

## Time Stop
- Swing trades: exit if no meaningful progress in **5–7 days**
- Multi-year base breakouts: **15–20 days** patience minimum
- If price is below entry after time stop and thesis hasn't fired → exit regardless of SL

## MTF-Specific Risk
- MTF = 3× leverage. A 10% adverse move = 30% position loss.
- Only A/A+ grade setups eligible for MTF
- SL on MTF positions must be within 8–10% of entry — mandatory

## Correlation Risk
- Current portfolio has MTF + defence sector concentration → **cascade risk** if sector rotates
- Never have >40% of portfolio in the same sector at the same time

## India-Specific Checks
- Watch US market close (spillover effect next morning)
- Rupee movement (INR depreciation = FII outflows = pressure)
- PCR (Put-Call Ratio) — above 1.0 = bullish sentiment; below 0.8 = caution
- Max pain level — watch weekly expiry (Thursday)
- Avoid new entries during earnings week for that specific stock

## Related
- [Entry Rules](/rules/entry-rules.md)
- [Exit Rules](/rules/exit-rules.md)
- [MTF Criteria](/frameworks/mtf-criteria.md)
- [BVM Framework](/frameworks/bvm.md)
