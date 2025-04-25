# 📌 Alpha: Analyst – EPS-to-Price Signal
🧮 Alpha Formula

rank(ts_rank(est_eps/close,60))

🧠 Hypothesis & Strategy

This alpha leverages the estimated EPS (Earnings Per Share) to price ratio as a signal of a company's earnings power relative to its market valuation.
- The est_eps/close ratio is a proxy for forward earnings yield — how much earnings investors expect to receive for every unit of price paid.
- A rising ratio suggests improving fundamentals (higher future earnings expectation or undervalued pricing).
- Conversely, a declining ratio might indicate reduced analyst confidence or overpriced stocks.

By applying a 60-day time-series rank to this ratio, we measure how strong the signal is relative to its past values. This temporal ranking helps identify sustained momentum in analyst sentiment and avoids noisy fluctuations.

Trading Logic: 
- Go long on stocks where the est_eps/close ratio has improved relative to the past 60 days — signaling growing confidence in future performance.
- Go short on those where the ratio is deteriorating — potentially overhyped or facing future earnings pressure.

📊 Performance Metrics

- Sharpe	0.61

- Turnover	16.71%

- Fitness	0.27

- Returns	3.37%

- Drawdown	3.58%

- Margin	4.03‱

Lower turnover and drawdown suggest that it could be suitable for more stable, low-volatility portfolios. 
