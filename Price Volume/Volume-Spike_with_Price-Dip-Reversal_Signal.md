# 📌 Alpha: Price-Volume – Volume Spike with Price Dip Reversal Signal
🧮 Alpha Formula

rank(volume / (ts_sum(volume,60)/60) * rank((ts_sum(close,5)/5) / close))

🧠 Hypothesis & Strategy

This alpha is based on a price-volume interaction signal that captures bullish sentiment driven by abnormal trading activity during a short-term price pullback.
- Volume Spike: This measures how today’s volume compares to its 60-day average. A value significantly >1 indicates unusual interest or activity, potentially from institutional investors or market-moving news.
- Short-Term Price Weakness: If this ratio is >1, it means the current price is below the recent 5-day average, indicating a pullback or temporary weakness.
- Combined Ranking: By multiplying the ranked volume spike with the ranked price drop, the alpha targets stocks that are experiencing surging volume alongside a recent price dip, which is often a bullish reversal signal.

This alpha is designed to identify accumulation phases, where there is increased market interest (rising volume), possibly hinting at smart money entry. Or, the price has temporarily dropped, creating a potential buying opportunity before a reversal. Such setups often precede price rebounds, especially when volume confirms that the market is absorbing the temporary sell-off.

📊 Performance Metrics

- Sharpe	2.27

- Turnover	22.75%

- Fitness	2.34

- Returns	24.08%

- Drawdown	3.39%

- Margin	21.17‱

Strong Sharpe and Fitness scores suggest excellent risk-adjusted performance and signal quality. Volume-based components add robustness against false breakouts by ensuring market participation confirmation.
