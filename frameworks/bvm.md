---
type: trading-framework
title: Brahma-Vishnu-Mahesh (BVM) Market Hierarchy
description: Three-tier market filter that determines whether it is safe to buy, hold, or stay in cash. Must be checked before any trade entry.
tags: [market-regime, nifty, sector, breadth, entry-filter]
timestamp: 2026-06-28T00:00:00Z
---

# Brahma-Vishnu-Mahesh (BVM) Framework

The tri-filter system that gates every trade. All three tiers must align before entering any new position.

## The Three Tiers

### Brahma — The Market (Non-Negotiable Gate)
The broader Indian market (Nifty 50 / Nifty 500).

| Signal | Verdict |
|--------|---------|
| Nifty in uptrend, above 200 EMA, VIX < 18, FII net buyers | ✅ Bullish — trades allowed |
| Nifty range-bound, VIX 18–22, mixed FII | ⚠️ Partial — only A+ setups |
| Nifty below 200 EMA, VIX > 22, FII heavy sellers | ❌ Bearish — no new entries |

**Rule: If Brahma is red, no new long entries regardless of how strong the stock looks.**

### Vishnu — The Sector
The sector the stock belongs to must be leading or at least neutral.

| Signal | Verdict |
|--------|---------|
| Sectoral index outperforming Nifty 50 on 1M + 3M basis | ✅ Leading |
| Sectoral index inline with Nifty | ⚠️ Neutral — acceptable |
| Sectoral index underperforming Nifty by >5% on 1M | ❌ Lagging — downgrade setup |

### Mahesh — The Stock
The individual stock's own technical and fundamental position.

| Signal | Verdict |
|--------|---------|
| Near ATH or 52-week high, base formed, King Candle confirmed | ✅ Strong |
| Mid-range, base forming, volume building | ⚠️ Developing |
| Below 200 EMA, distribution, falling volume | ❌ Avoid |

## Output Format
```
BRAHMA-VISHNU-MAHESH:
  Market: [Bull/Bear/Range]
  Sector: [Leading/Lagging/Neutral]
  Stock: [ATH/52wkH/Range]
  Verdict: ✅ Green / ⚠️ Partial / ❌ Red
```

## Key Data Inputs
- Nifty 50 / Nifty 500 price vs 200 EMA
- VIX level (India VIX)
- FII net buy/sell (daily, NSE data)
- PCR (Put-Call Ratio) — above 1 = bullish sentiment
- Sectoral index performance vs Nifty 50

## Related
- [Entry Rules](/rules/entry-rules.md)
- [King Candle](/frameworks/king-candle.md)
- [Risk Rules](/rules/risk-rules.md)
