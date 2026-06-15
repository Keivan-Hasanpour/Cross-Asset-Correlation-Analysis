# Cross-Asset Correlation Analysis

This project analyzes daily return correlations across major crypto, equity, commodity, and currency-market proxies. It downloads market data with `yfinance`, cleans missing values, calculates daily percentage returns, and visualizes the resulting correlation matrix with both Seaborn and Plotly heatmaps.

## Assets

| Asset | Yahoo Finance ticker | Market proxy |
| --- | --- | --- |
| Bitcoin | `BTC-USD` | Crypto |
| Ethereum | `ETH-USD` | Crypto |
| Gold Futures | `GC=F` | Commodity |
| S&P 500 ETF | `SPY` | U.S. equities |
| U.S. Dollar Index | `DX-Y.NYB` | Currency index |

## Project Files

- `Cross-Asset Correlation Analysis.ipynb`: main analysis notebook
- `requirements.txt`: Python package dependencies
- `.gitignore`: common Python/Jupyter files to exclude from Git

## How to Run

1. Clone the repository.
2. Create and activate a virtual environment.
3. Install the dependencies:

```bash
pip install -r requirements.txt
```

4. Open the notebook:

```bash
jupyter notebook "Cross-Asset Correlation Analysis.ipynb"
```

5. Run all cells from top to bottom.

## Methodology

The notebook follows these steps:

1. Define the asset universe and analysis window.
2. Download adjusted daily close prices from Yahoo Finance.
3. Forward-fill non-trading-day gaps and remove any remaining missing rows.
4. Convert prices to daily percentage returns.
5. Compute the Pearson correlation matrix.
6. Visualize correlations with static and interactive heatmaps.

## Interpreting Correlations

- A correlation close to `1` means two assets tended to move in the same direction.
- A correlation close to `0` means the relationship was weak or inconsistent.
- A correlation close to `-1` means two assets tended to move in opposite directions.

Correlation does not imply causation. Market relationships can change over time, especially during high-volatility regimes.

## Notes

- The end date is set dynamically to the current date when the notebook runs.
- Yahoo Finance data availability can vary by ticker and date.
- The analysis uses daily returns, not raw prices, because returns are more appropriate for comparing assets with different price scales.


