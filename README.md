# quantitative-portfolio-optimization
Financial modeling pipeline computing CAPM, Beta, and Sharpe/Treynor ratios to optimize a multi-asset equity portfolio.
# Quantitative Portfolio Optimization & CAPM Analysis

## 📌 Business Challenge
Investment decisions frequently over-index on historical returns while ignoring systematic risk and volatility. A purely return-focused strategy can destroy risk-adjusted value[cite: 182]. This project architects a mathematical framework to evaluate risk-return trade-offs and optimize capital allocation across a multi-asset portfolio.

## 🎯 Project Objective
To conduct a comprehensive risk-return analysis of three major Indian equities (HDFC Bank, TCS, Reliance Industries) against the NIFTY 50 benchmark over a 60-month horizon (Jan 2021 – Dec 2025)[cite: 181]. The analysis culminates in an evidence-based ₹10,00,000 investment allocation[cite: 183].

## ⚙️ Analytical Methodology & Tech Stack
* **Languages & Libraries:** Python, Pandas, NumPy, Matplotlib
* **Financial Modeling:** Calculated Annualized Risk (Standard Deviation), Beta, Covariance, Pearson Correlation, and the Capital Asset Pricing Model (CAPM) required rate of return[cite: 184].
* **Performance Metrics:** Evaluated risk-adjusted performance using the **Sharpe Ratio** and **Treynor Ratio**[cite: 184].
* **Cross-Validation:** Replicated and validated all programmatic Python outputs against native Microsoft Excel financial models to ensure formulaic integrity[cite: 182].

## 📊 Key Findings
* **The Risk-Return Disconnect:** TCS carried the highest annualized risk (21.18%) but yielded the lowest return (2.87%), resulting in a negative Sharpe Ratio (-0.1479) and proving that risk alone does not guarantee reward[cite: 185, 187].
* **Strongest Risk-Adjusted Asset:** Reliance Industries acted as the primary alpha generator, delivering the highest Sharpe Ratio (0.3711) and Treynor Ratio (6.49%) alongside a 13.49% annualized return[cite: 185].
* **Portfolio Optimization:** Compared a naive equal-weighted portfolio (Portfolio A) against an evidence-based allocation (Portfolio B). By minimizing exposure to risk-inefficient assets, Portfolio B generated a significantly higher Expected Return (10.59% vs 8.38%) and nearly doubled the Sharpe Ratio (0.2995 vs 0.1622) for a marginal 0.67 pp increase in absolute risk.

## 💡 Strategic Allocation
For a moderately risk-averse investor over a 5-year horizon, the recommended ₹10,00,000 allocation is:
* **40% HDFC Bank (₹4,00,000):** Defensive anchor (Lowest Risk: 16.97%, Beta: 0.89)[cite: 185, 197].
* **50% Reliance Industries (₹5,00,000):** Core growth engine (Highest Sharpe)[cite: 197].
* **10% TCS (₹1,00,000):** Minimal weighting retained strictly for correlation diversification[cite: 198].

## 📁 Repository Contents
* `portfolio_optimization.ipynb`: Python pipeline for covariance matrix calculation and portfolio metric generation.
* `CIA_2_FRA_SPREADSHEET (1).xlsx`: Excel-based financial model validating the programmatic CAPM and Sharpe calculations.
* `CIA_2_FRA_REPORT_ (1).pdf`: Executive summary detailing the investment thesis and mathematical trade-offs[cite: 176].
* `Datasets/`: 60-month historical closing prices for HDFC, TCS, Reliance, and NIFTY 50.
