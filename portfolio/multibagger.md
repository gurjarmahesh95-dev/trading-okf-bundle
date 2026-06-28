---
type: portfolio-snapshot
title: Multibagger Portfolio — June 2026
description: Long-term multibagger portfolio. Max 10 slots, delivery only, ₹5L per slot cap. Free-ride at 2× (sell half, cost basis → zero). 6/10 slots currently filled.
resource: https://supabase.com/dashboard/project/ukoyqdqgqqpdqklayasb
tags: [multibagger, long-term, delivery, free-ride, supabase]
timestamp: 2026-06-28T00:00:00Z
---

# Multibagger Portfolio

## Rules
- **Max stocks:** 10 (exit weakest to make room)
- **Per slot cap:** ₹5L maximum deployment
- **Free-ride trigger:** At 2× cost — sell FLOOR(shares/2), cost basis → zero, let rest run
- **Delivery only:** No MTF, no F&O on multibagger positions
- **Review cadence:** Quarterly health score + thesis check

## Current Holdings (6/10 slots)

| Slot | Symbol | Status | Free-Ride Progress |
|------|--------|--------|-------------------|
| 1 | ATHERENERG | Active | Monitoring |
| 2 | ATLANTAELE | Active | Monitoring |
| 3 | JAYBARMARU | Active | Monitoring |
| 4 | SYRMA | Active | Monitoring |
| 5 | ASMTECHLTD | Active | ~+35% — closest to 2× trigger. FY26 annual results due Jul 2026 |
| 6 | AEQUS | Active | (Position taken at loss — watchlist for reentry) |

**4 slots open.**

## Data Sources
- Live prices: INDmoney MCP (web search fallback for JAYBARMARU, ATHERENERG, ATLANTAELE, SYRMA, ASMTECHLTD)
- Fundamentals: screener.in (mandatory fetch before any workflow except price update)
- Events: BSE/NSE filing PDFs
- Storage: Supabase tables — `multibagger_portfolio`, `multibagger_buys`, `multibagger_health_scores`, `multibagger_events`, `multibagger_exits`

## Nine Workflows
A — Price Update | B — Add Buy | C — Log Event | D — Health Score | E — Portfolio Review | F — Add Stock | G — Results Deep-Dive | H — Thesis Invalidation | I — Exit Position

## Thesis Invalidation Triggers (General)
A multibagger position is exited when:
1. Management guidance reverses for 2+ consecutive quarters
2. Order book drops below critical threshold (stock-specific)
3. Sector tailwind is structurally broken (not cyclical)
4. Promoter pledging increases significantly (>30% pledged)
5. Free-ride is triggered — let it run at zero cost

## Related
- [Open Trades](/portfolio/open-trades.md) — JAYBARMARU appears in both
- [Watchlist](/portfolio/watchlist.md)
- [Supabase Schema](/infrastructure/supabase.md)
