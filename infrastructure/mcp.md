---
type: infrastructure
title: MCP Connections — Connected Tools
description: All MCP servers connected to the trading system. Capabilities, auth notes, and known limitations per connection.
tags: [MCP, tools, infrastructure, brokers, automation]
timestamp: 2026-06-28T00:00:00Z
---

# MCP Connections

## Trading & Market Data

### Supabase MCP
- **Project:** ukoyqdqgqqpdqklayasb
- **Use:** All database reads/writes (trades, multibagger, fronttest, posts)
- **Tool:** `Supabase:execute_sql`

### INDmoney MCP
- **URL:** https://mcp.indmoney.com/mcp
- **Use:** Live prices, OHLC, Indian stock details (read-only, no order placement)
- **Hardcoded IND keys:** SEDEMAC=INDS41627, EMMVEE=INDS39705, INOXINDIA=INDS28433, NETWEB=INDS26499
- **Fallback:** JAYBARMARU, ATHERENERG, ATLANTAELE, SYRMA, ASMTECHLTD → use web search (INDmoney unreliable for these)
- **Workflow:** `lookup_ind_keys` → `get_indian_stocks_details` / `get_indian_stocks_ohlc`

### Dhan MCP
- **URL:** https://mcp.dhan.co/mcp
- **Use:** Full read-write broker access (portfolio, orders, positions)
- **Auth:** Requires session auth each time (not persistent)
- **Limitations:** AMO (After Market Orders) not supported. Static IP whitelist required for live orders.

### Kite (Zerodha) MCP
- **URL:** https://mcp.kite.trade/mcp
- **Use:** Read portfolio, place orders on Zerodha

### FMP MCP
- **URL:** https://financialmodelingprep.com/mcp
- **Use:** Financial data, earnings, fundamentals

---

## Automation

### n8n MCP
- **URL:** https://n8n.maheshbuilds.tech/mcp-server/http
- **VPS:** Hostinger VPS (maheshbuilds.tech) with Traefik + Let's Encrypt SSL
- **Setup date:** June 23, 2026
- **Key webhooks:**
  - Doc writer: `https://n8n.maheshbuilds.tech/webhook/append-doc`
  - Actions: create, append, get, replace (field: `text`)
  - Google Docs Chat Agent workflow ID: `pkrBWXm8MsnbGDSK`

### Google Drive MCP
- **Use:** Trading journal (Google Docs), thesis documents, fronttest trackers
- **Journal ID:** `11lkl-2zcGaX9JmyoJm4O6OGVkDLw8n1Nzmgi0PekSto` (source of truth — V2 ID is outdated)
- **Fronttest files (in "Mahesh swing trackers" folder):**
  - IPO tracker: `1jRJrzmeEHVkXyLrdZoXgG8DkyW6mvhfzNPoz2J5OBLE`
  - Nifty500: `1PPpAePrEyLeNialmr9c6Vi512ZGrHzeay_qEYYRGEAc`
  - Microcap250: `1g6_fLWLjTspIlsCVyHJEayGJK8li9D7bMULhTtf3bLg`
  - **Read Priority Watchlist tab first before any trade ideas**

---

## Content & Productivity

### Gmail MCP | Canva MCP | Notion MCP | Zapier MCP
- Standard connections for content, email, and knowledge base

### Higgsfield MCP
- **URL:** mcp.higgsfield.ai/mcp
- **Status:** Currently experiencing authentication errors (as of Jun 2026)

---

## Related
- [Supabase Schema](/infrastructure/supabase.md)
- [n8n Workflows](/infrastructure/n8n.md)
- [Brokers](/infrastructure/brokers.md)
