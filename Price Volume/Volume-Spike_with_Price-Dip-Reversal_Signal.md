# 📌 Alpha: Price-Volume – Volume Spike with Price Dip Reversal Signal
🧮 Alpha Formula

rank(volume / (ts_sum(volume,60)/60) * rank((ts_sum(close,5)/5) / close))

🧠 Hypothesis & Strategy
This alpha is based on a price-volume interaction signal that captures bullish sentiment driven by abnormal trading activity during a short-term price pullback.
- Volume Spike:

  volume / (ts_sum(volume, 60)/60)

  This measures how today’s volume compares to its 60-day average. A value significantly >1 indicates unusual interest or activity, potentially from institutional investors or market-moving news.

- Short-Term Price Weakness:

  ts_sum(close,5)/5 / close

  If this ratio is >1, it means the current price is below the recent 5-day average, indicating a pullback or temporary weakness.

- Combined Ranking:

  By multiplying the ranked volume spike with the ranked price drop, the alpha targets stocks that are experiencing surging volume alongside a recent price dip, which is often a bullish reversal signal.
