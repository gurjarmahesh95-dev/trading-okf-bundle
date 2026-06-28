# Trading OKF Bundle

An [Open Knowledge Format (OKF)](https://cloud.google.com/blog/products/data-analytics/how-the-open-knowledge-format-can-improve-data-sharing) bundle of my complete Indian equity swing trading framework.

Built by [@equityos1](https://x.com/equityos1) | Kota, Rajasthan

---

## What is OKF?

Google's Open Knowledge Format (v0.1, Jun 2026) represents knowledge as a directory of markdown files with YAML frontmatter — readable by humans, AI agents, and any tool without a proprietary SDK.

This bundle converts my entire trading system into that format so any agent I use starts with full context.

---

## Bundle Structure

```
trading-okf-bundle/
├── index.md                    ← Start here
├── frameworks/
│   ├── bvm.md                  ← Brahma-Vishnu-Mahesh market hierarchy
│   ├── darvas-box.md           ← Box breakout (EOD only, never intraday)
│   ├── bamboo-method.md        ← Vijay Thakkar's multi-year base system
│   ├── king-candle.md          ← 2× volume institutional discovery signal
│   ├── lynch-filter.md         ← Peter Lynch fundamental screen (PEG <1)
│   └── mtf-criteria.md         ← 5 conditions for leveraged MTF entries
├── rules/
│   ├── entry-rules.md          ← 8-point pre-entry checklist
│   ├── exit-rules.md           ← 5 rules from real trade autopsies
│   ├── risk-rules.md           ← Position sizing, daily limits, time stops
│   └── violations.md           ← Hard-coded mistakes to never repeat
├── portfolio/
│   ├── open-trades.md          ← Live swing positions (Jun 2026)
│   ├── multibagger.md          ← Long-term portfolio (6/10 slots)
│   └── watchlist.md            ← Stocks on radar with entry zones
└── infrastructure/
    ├── supabase.md             ← Database schema (all 8 tables)
    └── mcp.md                  ← MCP connections (Dhan, Zerodha, INDmoney, n8n)
```

---

## The Framework

Three methods blended into one system:

- **Darvas Box** — tight consolidations, EOD breakouts, volume confirmation
- **Bamboo Method** (Vijay Thakkar) — multi-year bases, Double Engine signal, King Candles
- **Peter Lynch** — PEG <1, one-sentence thesis, rising institutional ownership

Gated by the **BVM hierarchy** (Brahma = market, Vishnu = sector, Mahesh = stock). All three must align before entry.

---

## Why OKF?

Every AI agent I use — for trade analysis, journal review, n8n automation — now reads this bundle before responding. No re-explaining. No context loss. The framework travels with the knowledge.

---

## Disclaimer

Not a SEBI registered Research Analyst. Nothing here is investment advice. I hold positions mentioned in portfolio files. DYOR.
