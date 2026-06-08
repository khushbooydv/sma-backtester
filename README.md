# SMA Backtester - US Stock Market Analysis
I built this project to understand whether a simple moving average crossover strategy can consistently beat a buy-and-hold approach over a long period.
Stocks analyzed: AAPL, SPY, KO, IBM, DIS, MSFT (2014-2024).

----

## What this Project covers
- Downloaded real historical price data using yfinance.
- Normalized prices to compare all 6 stocks on the same scale.
- Calculated daily returns, log returns, variance, and annualized volatility.
- Built rolling SMA windows (10, 50, 200 day) on SPY.
- Performed drawdown analysis on AAPL - worst drawdown was in april 2020.
- Built two SMA crossover strategies:
  -> Strategy 1: Long/Short (Position = +1 or -1).
  -> Strategy 2: Long only (Position = +1 or 0).
- Compared annualized volatility: Strategy 1 = 30.6% vs Strategy 2 = 24.8%.
- Built a reusable test_strategy() function.
- Built SMABacktester class with plot_results() visualization.

----

## Key Findings
- Strategy 2 (long only) showed lower volatility than strategy 1 (long/Short).
- SMABacktester class tested on SPY using SMA 50/100 crossover.
- The SMABacktester class makes it easy to test any stock with any SMA window.

----

## How to run
```bash
pip install yfinance pandas numpy matplotlib seaborn
```
Open "sma_backtester.ipynb" in Jupyter Notebook and run cells sequentially.

----

## Stack
Python 3.11 · yfinance · pandas · numpy · matplotlib · seaborn
Data: Yahoo Finance | Built in Jupyter Notebook on Chromebook Linux

---

**Learning Project. Not Financial Advice**

