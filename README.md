# Algorithmic Trading Intro

Three guided projects from **freeCodeCamp's algorithmic trading course**, each building a stock screener in Python that turns market data into a buy list and exports it to Excel.

## Projects

| Notebook | Strategy | What it does |
|---|---|---|
| `equal_weighted_sp500.ipynb` | **Equal-weight S&P 500** | The S&P 500 is market-cap weighted. This version gives every constituent the same weight, spreading risk across sectors and away from the largest names, and computes how many shares of each to buy for a given portfolio size. |
| `quantitative_momentum.ipynb` | **Momentum screener** | Ranks stocks by one-year price return and return percentile, building toward a "high-quality momentum" (HQM) score, then sizes an equal-weight position in the top names. |
| `quantitative_value.ipynb` | **Value screener** | Looks for stocks trading below perceived intrinsic value using valuation multiples, starting with the price-to-earnings ratio. The course's composite approach combines P/E, P/B and P/FCF, since each ratio has its own blind spots. |

## Algo trading basics (course notes)

- An algorithm makes the investment decisions; strategies differ mainly in execution speed.
- Major players include Renaissance Technologies, AQR and Citadel Securities.
- Python is mostly "glue" around fast numerical libraries such as NumPy (written in C).
- The process: **collect data → form a strategy hypothesis → backtest it.**

## Running it

The notebooks pull market data from the Yahoo Finance API at yfapi.net. Put your API token in a local `secret_case.py`:

```python
API_TOKEN = "your_token_here"
```

Keep that file out of version control. Then:

```bash
pip install pandas numpy requests scipy xlsxwriter
jupyter notebook
```

## Tech stack

Python · pandas · NumPy · SciPy · requests · XlsxWriter
