---
type: infrastructure
title: Supabase Schema — Trading Database
description: All Supabase tables used across swing trading, multibagger, fronttest, and content workflows. Project ID ukoyqdqgqqpdqklayasb.
resource: https://supabase.com/dashboard/project/ukoyqdqgqqpdqklayasb
tags: [supabase, database, schema, infrastructure]
timestamp: 2026-06-28T00:00:00Z
---

# Supabase Schema

**Project ID:** `ukoyqdqgqqpdqklayasb`
**Tool:** `Supabase:execute_sql` for queries | `Supabase:apply_migration` for DDL

---

## Swing Trading Tables

### `open_trades`
Active swing positions. Source of truth for current portfolio state.
Key columns: symbol, qty, avg_price, sl, t1, t2, t3, entry_date, trade_type (delivery/MTF), thesis

### `closed_trades`
All completed trades with entry, exit, P&L, and exit reason.
Key columns: symbol, qty, buy_price, sell_price, pnl, exit_reason, exit_date

### `fronttest`
Paper trades for testing new setups without real capital.
Key columns: symbol, entry_price, sl, t1, t2, status, thesis, result_notes

### `posts`
X (Twitter) content drafts and published posts.
Key columns: ticker, content, status (draft/published/scheduled), trigger_condition, hook_type

---

## Multibagger Tables

### `multibagger_portfolio`
One row per stock — master record with cost basis, free-ride status, thesis.

### `multibagger_buys`
Every SIP or lumpsum buy entry per stock.

### `multibagger_health_scores`
Quarterly health score snapshots (0–100 score per stock).

### `multibagger_events`
BSE filings, catalysts, red flags, news events per stock.

### `multibagger_exits`
Full and partial exits with realised P&L.

---

## Known Data Corrections
- **JAYBARMARU:** 333 shares @ ₹137.45 (corrected — use this, not any earlier figure)
- **NETWEB:** Current position is 23 shares @ ₹5,081.66. Previous 80-share position is CLOSED.

---

## Related
- [Open Trades](/portfolio/open-trades.md)
- [Multibagger Portfolio](/portfolio/multibagger.md)
- [n8n Workflows](/infrastructure/n8n.md)
- [MCP Connections](/infrastructure/mcp.md)
