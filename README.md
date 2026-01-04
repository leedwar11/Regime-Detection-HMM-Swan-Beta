# Regime Detection with HMM (Public Demo) — Tail-Risk Proxy

## Overview
This repository presents a **public, reproducible demo** of a market **regime detection** workflow using **Hidden Markov Models (HMMs)**.  
The core idea is to identify latent market states and study how **risk dynamics** differ across regimes using **tail-risk proxies** (e.g., rolling CVaR).

## Note on Confidentiality
This project is inspired by research conducted during a research internship.  
The original work incorporated **proprietary “Swan Beta” tail-risk features** and **internal datasets**. To comply with confidentiality requirements, this public version:
- replaces proprietary components with **open, standard tail-risk proxies** (e.g., rolling CVaR / drawdown / realized volatility),
- uses **public market data only**, and
- omits any confidential implementation details, data sources, or performance artifacts.

## Methodology
1. **Data & Returns**
   - Load public price data and compute returns.

2. **Tail-Risk Proxy Construction (Public)**
   - Construct open proxies that capture downside risk (e.g., rolling CVaR at 5%, max drawdown, realized volatility).

3. **HMM Regime Inference**
   - Fit an HMM to selected observable features (e.g., returns + tail-risk proxy).
   - Infer regimes and regime probabilities.

4. **Regime Diagnostics**
   - Transition matrix and state persistence.
   - Regime-conditioned risk characteristics (e.g., CVaR/volatility by regime).
   - Visualizations of regimes over time.
## How to Run
```bash pip install -r requirements.txt ````Open the notebookto reproduce the analysis.

## Outputs
- Regime assignments and regime probabilities
- Transition matrix / persistence diagnostics
- Regime-conditioned risk summaries and plots

## Disclaimer
This repository is for **research and educational demonstration** purposes only and does not constitute investment advice.
