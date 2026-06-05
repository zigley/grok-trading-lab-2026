# Stock Bots + Wheel Strategy + Option Bots Batch (365d + Current Chains)
**Generated: 2026-06-05 by Money Making Grok trading module (paper sims only)**

**NOT FINANCIAL ADVICE. Past performance does not predict future results. Trading involves substantial risk of loss. This is paper simulation only. You can lose money.**

Created with assistance from Grok (xAI) AI tools. Content synthesized for educational/actionable value; verify independently. All runs use public historical data (yfinance) + live snapshot chains. No real orders, no keys used.

## Executive Summary
- **15 stock directional paper bots** (MA crossover, RSI, Bollinger) on 6 equities (AAPL, NVDA, TSLA, SPY, AMD, MSFT), 365 days via PaperBroker (slippage, fees, realistic fills/sizing).
- **4 wheel strategy paper bots** (CSP -> assignment -> CC cycle) on AAPL/SPY/TSLA/NVDA, 365d, ~30d cycles, ~1.8% target prem per cycle (1-share equiv units; scale x100 for standard contracts).
- **5+ option income paper bots** (current yfinance option chain snapshot for OTM CSP + CC legs), multiple underlyings x1-2 contracts. PnL modeled as +premium if OTM expiry (max credit profit); full downside risk disclosed.
- **Aggregate simulated P&L from this batch: +~47,031** (directional stock ~+36,957; wheels ~+292 scaled; options premiums ~+9,782). Ledger total sim now ~$108k+ (compounds prior forex + sales + equity wins).
- All logged to `ledger.json` (trade type), plots + per-bot trade JSONs in `products/`.
- **Key takeaway (paper only)**: In the specific 2025-2026 historical window, trend-following captured massive equity upside on volatile names. Wheel provided steady (small-scale) credit harvesting with occasional assignments. Current-chain options showed attractive near-term premiums on high-IV names but are snapshots — not multi-year backtests.

See full details + run instructions in the dedicated launch repo: https://github.com/zigley/grok-stock-wheel-options-bots-2026

**Run the machine:** `python -m money_grok trading simulate --symbol SPY --days 365 --strategy wheel -- or options`