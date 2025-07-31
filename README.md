# NSE Mean Reversion Quantitative Trading Strategy

A backtested, portfolio-based mean reversion strategy developed and optimized for the Indian stock market (NSE). This project demonstrates the iterative process of building a quantitative trading model, from a simple idea to a robust, profitable system.

### The Problem

The initial hypothesis was that stock prices revert to their historical mean. A simple strategy was built using Bollinger Bands and the Relative Strength Index (RSI). Initial backtests revealed a critical flaw: the strategy was highly susceptible to major losses during trending markets and black swan events (like the COVID-19 crash).

### The Solution: A Refined and Robust System

To address the strategy's flaws, a multi-stage optimization process was implemented:

1.  **Market Regime Filter:** A filter was introduced using a long-term moving average to ensure the strategy only trades in non-trending (range-bound) markets.
2.  **Dynamic Stop-Loss:** A fixed-percentage stop-loss was replaced with a dynamic stop-loss based on the stock's Average True Range (ATR), allowing the strategy to adapt to volatility.
3.  **Parameter Optimization:** Through iterative testing, the optimal parameters were found that balanced safety and opportunity, turning a loss-making strategy into a highly profitable one.

### Key Performance Metrics (Portfolio-based Backtest)

The final strategy was backtested on a portfolio of 60+ stocks from the NSE Nifty 100 over a 4.5-year period (2020-2024).

* **Total trades across portfolio:** 42
* **Cumulative Return:** 143.12%
* **Win Rate:** 76.19%

<img width="341" height="78" alt="image" src="https://github.com/user-attachments/assets/ae1a8c5c-303b-4500-b78f-1383d13864d2" />


### How to Run

1.  Clone this repository.
2.  Install the required Python libraries: `yfinance`, `pandas`, `ta`, `matplotlib`.
3.  Run the `portfolio_backtest.py` script.

### Future Work

* Integrate with a professional backtesting library like `backtrader` for more detailed metrics (Sharpe Ratio, Max Drawdown).
* Expand the strategy to include more tickers and explore different market sectors.
* Explore alternative entry/exit signals beyond Bollinger Bands and RSI.

---

sYanXO
