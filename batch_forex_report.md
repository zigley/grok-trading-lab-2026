# Batch Forex Simulations Report
Generated: 2026-06-05 (Money Making Grok trading module)
**NOT FINANCIAL ADVICE. Past performance does not predict future results. Trading involves substantial risk of loss. This is paper simulation only.**

## Pairs Tested
EURUSD=X, GBPUSD=X, USDJPY=X, AUDUSD=X, EURGBP=X

## Strategies
ma_crossover, rsi (90 days each)

## Results (PnL in USD sim)
- EURUSD=X ma_crossover: -58.65 (1 trade)
- EURUSD=X rsi: 0.0 (0 trades)
- GBPUSD=X ma_crossover: +6.04 (1 trade)
- GBPUSD=X rsi: 0.0 (0 trades)
- USDJPY=X ma_crossover: 0.0 (0 trades)
- USDJPY=X rsi: 0.0 (0 trades)
- AUDUSD=X ma_crossover: -117.56 (1 trade)
- AUDUSD=X rsi: +396.84 (2 trades)
- EURGBP=X ma_crossover: 0.0 (0 trades)
- EURGBP=X rsi: -43.44 (1 trade)

**Aggregate P&L: +183.23**

## Logged
All individual and aggregate recorded in ledger.json as 'trade' entries with timestamps.
Total sim capital updated accordingly.

## Notes
- Some 0s due to no signal triggers in the 90d window.
- Plots saved in products/ for active ones.
- PaperBroker used for execution simulation.
- All via public yfinance data.

See money_grok/trading/ for code, strategies, paper broker.

Run: python -m money_grok trading simulate --symbol EURUSD=X --days 90 --strategy ma_crossover
