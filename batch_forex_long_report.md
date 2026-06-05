# LONG Batch Forex Simulations Report (365 days)
Generated: 2026-06-05 (Money Making Grok trading module)
**NOT FINANCIAL ADVICE. Past performance does not predict future results. Trading involves substantial risk of loss. This is paper simulation only.**

## Setup
- Pairs: EURUSD=X, GBPUSD=X, USDJPY=X, AUDUSD=X, EURGBP=X
- Strategies: ma_crossover, rsi, bollinger
- Period: 365 days each (15 total sims)
- Engine: simulate_paper_bot + PaperBroker (simulated fills, 0.1% fee/slippage model, position sizing)
- Data: public yfinance historical
- All logged to ledger.json as 'trade' entries (timestamped)

## Results (PnL in USD sim)
- EURUSD=X ma_crossover: -70.15 (1 trade)
- EURUSD=X rsi: 451.27 (8 trades)
- EURUSD=X bollinger: 228.91 (9 trades)
- GBPUSD=X ma_crossover: -29.61 (1 trade)
- GBPUSD=X rsi: 67.25 (6 trades)
- GBPUSD=X bollinger: 216.76 (7 trades)
- USDJPY=X ma_crossover: 724.0 (1 trade)
- USDJPY=X rsi: 234.41 (2 trades)
- USDJPY=X bollinger: 410.15 (3 trades)
- AUDUSD=X ma_crossover: 611.64 (1 trade)
- AUDUSD=X rsi: 565.82 (4 trades)
- AUDUSD=X bollinger: 431.8 (5 trades)
- EURGBP=X ma_crossover: -18.95 (1 trade)
- EURGBP=X rsi: 69.03 (7 trades)
- EURGBP=X bollinger: 80.44 (4 trades)

**Aggregate P&L from LONG batch: 3972.77**

## Logged to ledger
- 15 individual long-batch entries
- 1 aggregate FOREX_BATCH_LONG +3972.77
- Current grand total sim: ~12718 (includes prior)

## Artifacts
- Plots in products/ (e.g. paper-bot-EURUSD=X-*.png etc.)
- Trade logs: paper_bot_trades_*.json
- This report

## Key Observations (paper only)
- Longer window captured trends: strong positive on USDJPY/AUDUSD.
- RSI/Bollinger triggered more trades than simple MA.
- Still simulation: past results do not predict future. No live trading.

See money_grok/trading/ for code.

Run: python -m money_grok trading simulate --symbol EURUSD=X --days 365 --strategy rsi