# Portfolio Optimisation & CAPM Analysis: HDFC Bank, TCS, Reliance

A Python risk–return analysis of three large Indian stocks against the NIFTY 50, ending in an evidence-based ₹10 lakh allocation. Every result is cross-checked against an independent Excel model.

## Business challenge
Investors often chase past returns and ignore volatility and market risk. The aim is to compare the three stocks on a risk-adjusted basis and build a better portfolio than a naive equal split.

## Data
60 monthly closing prices (Jan 2021 – Dec 2025) for HDFC Bank, TCS, Reliance Industries and the NIFTY 50, in `data/`.

## Method
- Monthly returns, annualised return and risk (standard deviation)
- Covariance, Pearson correlation and **beta** against the NIFTY 50
- **CAPM** required return, **Sharpe** and **Treynor** ratios (risk-free rate 6%)
- Equal-weight portfolio (A) versus an evidence-based allocation (B)
- **Excel cross-validation:** every Python metric is reproduced in `reports/excel_validation_model.xlsx` (sheet *Excel Vs Python*).

## Key findings
- **Risk without reward:** TCS had the highest risk (21.18%) but the lowest return (2.87%), giving a negative Sharpe ratio (−0.148).
- **Best risk-adjusted stock:** Reliance had the highest Sharpe (0.371) and Treynor (6.49%) ratios, with a 13.49% annualised return.
- **Better portfolio:** Portfolio B raised expected return from 8.38% to 10.59% and nearly doubled the Sharpe ratio (0.162 → 0.300) for only 0.67 pp more risk.

## Recommended ₹10 lakh allocation (moderately risk-averse, 5-year horizon)
| Stock | Weight | Amount | Role |
|---|---|---|---|
| Reliance Industries | 50% | ₹5,00,000 | Growth engine (highest Sharpe) |
| HDFC Bank | 40% | ₹4,00,000 | Defensive anchor (lowest risk 16.97%, beta 0.89) |
| TCS | 10% | ₹1,00,000 | Kept for diversification |

*Coursework analysis on historical data; not investment advice.*

## Repository structure
```
├── portfolio_optimization.ipynb        # Full analysis with outputs
├── data/                               # Monthly prices: HDFC, TCS, RELIANCE, NIFTY50
└── reports/
    ├── report.pdf                      # Written report
    └── excel_validation_model.xlsx     # Excel model used to validate the Python results
```

## How to run
```bash
pip install -r requirements.txt
jupyter notebook portfolio_optimization.ipynb
```
Run from the repository root. A clean re-run reproduces every number in the notebook exactly.

## Tech stack
Python · pandas · NumPy · Matplotlib · Microsoft Excel
