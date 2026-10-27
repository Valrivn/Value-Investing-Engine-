# Value Investing Engine

> **A Systematic Equity Research Project on Economic Value, Market Noise, and Empirical Falsification**

* **Live Site:** [https://valrivn.github.io/Value-Investing-Engine-/](https://valrivn.github.io/Value-Investing-Engine-/)
* **Core Research Codebase & Data:** [https://github.com/Valrivn/Quant](https://github.com/Valrivn/Quant)

---

## Overview

**Value Investing Engine** is an independent quantitative research project investigating whether discretionary Value Investing frameworks (Benjamin Graham, Warren Buffett, Aswath Damodaran) can be systematically automated in Python. 

The engine evaluates whether combining quantitative balance sheet fundamentals with qualitative business durability indicators can generate genuine risk-adjusted alpha against the S&P 500, rather than relying on uncompensated market momentum.

### Methodological Focus & Data Integrity:
* **Zero Lookahead Bias:** All corporate filings are indexed strictly to official SEC publication timestamps (`filed_date`), eliminating the common flaw of trading on restated statements.
* **Strict Fail-Closed Architecture:** Assets with missing accounting metrics or unverified dates are excluded immediately, rejecting synthetic imputation and placeholder defaults.
* **Realistic Execution Friction:** Incorporates dynamic square-root market impact slippage and 15% turnover hysteresis deadbands to penalize portfolio churn.
* **100% Official Public APIs:** All data is ingested via official government and institutional REST endpoints (SEC EDGAR, Federal Reserve FRED, USPTO PatentsView, and CFPB Open Data) with zero web scraping.

---

### Empirical Findings (2018–2024 Walk-Forward, 83 Months Net):

| Metric | Sanitized Engine (Arm 1) | S&P 500 Benchmark (SPY) |
| :--- | :---: | :---: |
| **Annualized Return (CAGR)** | **11.57%** | 13.00% |
| **Market Sensitivity (Beta &beta;)** | **0.63** | 1.00 |
| **Down-Market Capture** | **64.3%** | 100.0% |
| **Maximum Drawdown** | **-17.78%** | -23.93% |
| **Sortino Ratio** | **1.13** | 1.04 |
| **Data Policy** | **Fail-Closed (Immediate Drop)** | Index Baseline |

While the baseline S&P 500 achieved an annualized return of 13.00% with a &minus;23.93% maximum drawdown, the sanitized engine achieved 11.57% CAGR while reducing systematic market sensitivity to a **0.63 Beta**, limiting maximum drawdown to **&minus;17.78%**, and capturing only **64.3% of the benchmark's losses** during down months.
