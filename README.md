# Technical Analysis of Stocks — MA Crossover Strategy (S&P 500)

This repository is dedicated to the technical analysis of stock prices using Python, starting with a moving average crossover strategy applied to the S&P 500 index (^GSPC). It represents my first public exploration of financial data analysis, and I plan to further expand and refine the code as my learning progresses.

## 📊 Strategy Overview

The current strategy evaluates the effectiveness of **moving average crossovers** in generating trading signals, comparing two approaches:

- **Long-only strategy**: Go long when the short-term MA crosses above the long-term MA, otherwise hold cash.
- **Long/Short strategy**: Go long on bullish crossovers, and go short on bearish ones.

Both strategies are benchmarked against a **Buy & Hold** strategy.

## 🧮 Methodology

- Data source: Yahoo Finance (`yfinance`)
- Underlying: S&P 500 Index (^GSPC)
- Period: January 2010 – December 2024
- Parameters: All combinations of short and long MA windows from 1 to 300 (excluding short ≥ long)
- Metrics: **Cumulative Return** and **Excess Return** over Buy & Hold
- Visualization: 3D surface plots using `matplotlib` and `mpl_toolkits.mplot3d`

## 📈 Results

The heatmaps below show excess returns relative to a Buy & Hold strategy:

### Long-only strategy  
![Long-only result](./long_only_plot.png)

### Long/Short strategy  
![Long/Short result](./long_short_plot.png)

## 🚀 What's Next

This is just the beginning. I'm planning to:
- Add Sharpe ratio and volatility evaluation
- Try other indicators (RSI, MACD, Bollinger Bands)
- Implement backtesting frameworks (e.g., `backtrader`)
- Explore portfolio optimization and ML-based strategies

## 🛠️ Technologies Used

- Python 3
- pandas
- numpy
- matplotlib
- yfinance

