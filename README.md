# Market-Neutral, But Is It Profitable? — Pairs Trading on the S&P 500

Final project for **Financial Markets Analytics (FDS01Q007)** — Prof. G. Forte, MSc Data Science, Unimib.
Implementation of Gatev, Goetzmann & Rouwenhorst (2006) pairs trading on S&P 500 monthly data (1991–2018).

**Method:** rolling 12-month formation / 6-month trading cycles → Engle-Granger cointegration on ~503,500 pairs/cycle, BH-FDR correction (5%), half-life filter (≤3 months) → top 20 pairs/cycle → z-score backtest (entry 2≤|z|<3) → equal-weight buy-and-hold benchmark comparison.

**Results:**

| | Ann. Return | Sharpe | Max DD |
|---|---|---|---|
| Benchmark | 7.90% | 0.453 | −61.3% |
| Strategy (V1/V2) | −0.61% / 0.06% | −0.138 / 0.021 | −26.1% / −13.9% |

**Finding:** the strategy is mechanically market-neutral but not profitable — consistent with the Do & Faff literature on post-2002 decline in pairs trading returns.

