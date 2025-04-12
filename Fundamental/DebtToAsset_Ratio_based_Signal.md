# 📌 Alpha: Fundamental – Debt/Asset Ratio-Based Signal

🧮 Alpha Formula

rank(ts_delta(debt,250)/assets && ts_delta(close,250) && ts_rank(-debt/equity,250))

🧠 Hypothesis & Strategy

This alpha ranks companies based on:

- Debt/Asset Ratio Delta: Measures how the debt-to-asset ratio has changed over the past year to assess financial leverage trends.

- Closing Price Trend: Captures price momentum by analyzing the change in closing price over 250 days.

- Debt/Equity Ratio Rank: Assesses financial stability by inversely ranking the debt/equity ratio — favoring companies with lower leverage.

Idea:
The goal is to identify companies:

- Efficiently using debt to fund growth (healthy debt/asset trend),

- Generating returns (positive price momentum),

- Financially stable (low debt/equity ratio).

Trading Logic:
Go long on companies with favorable scores across all metrics, and short those with weak fundamentals and poor momentum signals.

📊 Performance Metrics

- Sharpe = 0.57

- Turnover = 21.82%

- Fitness = 0.36

- Returns = 8.70%

- Drawdown = 14.30%

- Margin = 7.97‱

The use of combined ranking and time-series delta functions captures both temporal shifts and relative performance. Good balance between risk and return with moderate Sharpe and manageable drawdown.


