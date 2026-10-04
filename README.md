# NVDA Value at Risk Analysis

A Python-based analysis of NVIDIA (NVDA) downside risk, comparing Historical, Parametric Normal, and Monte Carlo Value at Risk (VaR).

## View the Reports

Open the reports below to view the Python code, charts, and calculated results directly in your browser. No installation is required.

- [Historical VaR Report](https://helen-siqi-he-nyu.github.io/nvda-value-at-risk-analysis/VaR_Historical_Clean.html)
- [Parametric Normal VaR Report](https://helen-siqi-he-nyu.github.io/nvda-value-at-risk-analysis/VaR_Parametric_Normal_Clean.html)
- [Monte Carlo VaR Report and Comparative Discussion](https://helen-siqi-he-nyu.github.io/nvda-value-at-risk-analysis/VaR_Monte_Carlo_Clean_v2%20%281%29.html)

## Project Scope

- Analyzed NVDA adjusted closing prices using a 2021–2025 sample window.
- Estimated VaR at 95% and 99% confidence levels.
- Compared daily and 30-trading-day risk for a hypothetical $100,000 NVDA position.
- Generated 100,000 Monte Carlo simulations with a fixed random seed.
- Visualized return distributions and downside thresholds.
- Discussed tail risk, model assumptions, and the impact of compounding.

## Methods

| Method | Daily VaR | 30-Day VaR |
| --- | --- | --- |
| Historical | Empirical quantiles of observed daily returns | Quantiles of rolling compounded returns |
| Parametric Normal | Analytical Normal quantiles using estimated mean and volatility | Normal approximation using mean and volatility scaling |
| Monte Carlo | Quantiles of simulated Normal daily returns | Quantiles of compounded simulated return paths |

## Selected Findings

- At 99% confidence, daily loss thresholds were approximately $7,740 under Historical VaR, $7,390 under Parametric Normal VaR, and $7,446 under Monte Carlo VaR.
- Daily Monte Carlo and Parametric estimates were close because both used the same Normal return model.
- Their 30-day estimates differed because Monte Carlo compounded daily returns, while the Parametric method used an additive Normal approximation.
- The comparison illustrates how distributional assumptions and calculation methods affect estimated downside risk.

Dollar figures above are presented as positive loss magnitudes. The reports display VaR as negative return and dollar thresholds. VaR is a quantile-based threshold, not a maximum possible loss.

## Tools

Python · pandas · NumPy · SciPy · Matplotlib · yfinance

## Context

Academic coursework project presented as a financial analysis work sample. The repository contains exported HTML notebooks with saved code, visualizations, and results.
