# Forex Batch Analysis: Which Strat/Pair "Won"? (365d sims)
Generated: 2026-06-05 (Money Making Grok trading module)
**NOT FINANCIAL ADVICE. Past performance does not predict future results. Trading involves substantial risk of loss. This is paper simulation only.**

## Summary of Batch
5 pairs x 3 strats = 15 sims, 365 days, using PaperBroker (sim fills, fees, sizing).
Aggregate P&L: +3972.77 (very positive in this historical window).

## Top Performers

**By Absolute PnL (biggest winners):**
1. USDJPY=X ma_crossover: +724.00 (1 trade, +724 per trade)
2. AUDUSD=X ma_crossover: +611.64 (1 trade, +611.64 per trade)
3. AUDUSD=X rsi: +565.82 (4 trades, +141.46 per trade)

**By PnL per Trade (efficiency, ignoring trade count):**
1. USDJPY=X ma_crossover: 724.00
2. AUDUSD=X ma_crossover: 611.64
3. AUDUSD=X rsi: 141.46

**By Strategy Totals (across all pairs):**
- ma_crossover: +1216.93 total (5 trades, avg +243.39 per trade) - Selective, high reward/risk. Big wins on trending pairs but few signals.
- rsi: +1387.78 total (27 trades, avg +51.40 per trade) - Most active, consistent positives.
- bollinger: +1368.06 total (28 trades, avg +48.86 per trade) - Similar to RSI, slightly more trades.

**By Pair Totals (sum of 3 strats):**
1. AUDUSD=X: +1609.26 (10 trades) - Clear winner. Strong trends captured well by all strats.
2. USDJPY=X: +1368.56 (6 trades) - Excellent, especially MA.
3. EURUSD=X: +610.03 (18 trades) - Solid, RSI/Bollinger carried it.
4. GBPUSD=X: +254.40 (14 trades) - Modest.
5. EURGBP=X: +130.52 (12 trades) - Weakest (perhaps more range-bound).

## Key Insights (Paper Only)
- **MA Crossover "won" the big individual scores** on USDJPY and AUDUSD — these pairs had clear trends in the 365d period where MA caught big moves with minimal trades. High PnL but low activity; vulnerable to whipsaws in choppy markets.
- **RSI and Bollinger "won" on volume/activity** — 27-28 trades vs MA's 5. Better for capturing smaller moves, more opportunities, lower per-trade but higher total in mixed conditions. Good for bots that want frequent signals.
- **AUDUSD=X and USDJPY=X dominated** — Commodity/AUD and safe-haven/JPY flows likely drove trends. EUR pairs more mixed (EURUSD decent, EURGBP poor).
- **Overall**: In this specific historical window, a MA-focused bot on AUD/USD/JPY would have "won" big. But RSI/Bollinger provided more balanced, trade-rich results. Diversify strats/pairs in real bots. No guarantee future similar.
- Trade count as proxy for opportunity: Bollinger/RSI >> MA.
- Risk note: Many "wins" from 1-2 big trades; drawdowns not analyzed here (would need full equity curves).

## Recommendations for Trading Bot Focus
- For high-conviction trending forex (JPY, AUD crosses): Prioritize MA crossover with filters (e.g. ADX for trend strength).
- For active trading/mean-reversion: RSI or Bollinger — more signals, easier position sizing.
- Portfolio: Allocate across pairs (avoid over-concentration in one like AUDUSD).
- Enhance: Add risk management (stops, position sizing by volatility), multi-timeframe, combine with crypto/PM signals.
- Next: Run with bollinger on more pairs, or add walk-forward validation, or live paper via ccxt (user keys + risk ack required).

## Data Source
From the 365d batch run. Full details + plots in products/ and previous batch_forex_long_report.md.
All sim/paper, logged to ledger (total sim now ~12718 including this batch's +3972.77).

See money_grok/trading/ for the bot code.
Run your own longer/more: python -m money_grok trading simulate --symbol USDJPY=X --days 730 --strategy ma_crossover

**NOT FINANCIAL ADVICE.** This is historical sim analysis only for the machine's development/education. Verify independently. Past != future.