# 📌 Alpha: Analyst – EPS Momentum with Conditional Mean Reversion
🧮 Alpha Formula

est_epsr > last_diff_value(est_epsr,20) 
    ? ts_rank(est_eps/close,60) 
    : rank(-ts_delta(close,5))

🧠 Hypothesis & Strategy

This alpha leverages earnings-per-share (EPS) revisions and short-term price behavior to adaptively decide between two different trading strategies based on analyst sentiment.
- Condition Check: If the current estimated EPS revision ratio (est_epsr) is higher than its value 20 days ago, it suggests analysts are becoming more optimistic about a company's future earnings.
- If True – Earnings Momentum Strategy: Rank the stock based on the ratio of estimated EPS to price (est_eps/close) over the past quarter (60 days). This identifies undervalued companies with strong earning potential, as high EPS relative to price often indicates a good value opportunity.
- If False – Mean Reversion Strategy: If analyst sentiment is not improving, fall back to a short-term mean reversion strategy, using the negative delta of the past 5 days' close. This captures stocks that may have overreacted to negative sentiment or market noise and are likely to revert.

The alpha switches between forward-looking analyst sentiment and price-based reversal, making it responsive to both fundamental outlook and technical movement.
It aims to:
- Exploit undervaluation when analysts revise estimates upwards.
- Avoid chasing weak fundamentals, instead focusing on technical correction when sentiment is flat or declining.

📊 Performance Metrics
- Sharpe	1.67
  
- Turnover	34.13%

- Fitness	0.89

- Returns	9.76%

- Drawdown	3.76%

- Margin	5.72‱

Combines fundamental momentum with short-term technical mean reversion. Strong Sharpe and low drawdown highlight balanced risk-adjusted performance.

