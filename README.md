# Regime Detection with HMM (Public Demo) — Tail-Risk Proxy

## Overview
This repository presents a **public, fully reproducible demo** of a market **regime detection** workflow using **Hidden Markov Models (HMMs)**.

The goal is to identify latent market regimes and analyze how **risk dynamics differ across regimes**, with a focus on **tail-risk behavior**.  
To ensure reproducibility and confidentiality compliance, this demo relies exclusively on **public data** and **standard, transparent risk proxies**.

---

## Note on Confidentiality
This project is inspired by research conducted during a research internship.

The original internal research incorporated **proprietary “Swan Beta” tail-risk measures**, internal coverage universes, and non-public datasets.  
To comply with confidentiality requirements, this public demo:

- replaces proprietary features with **open, standard tail-risk proxies** (e.g., rolling CVaR, drawdown, realized volatility),
- uses **public market data only** (via standard data providers),
- omits any confidential data sources, internal signals, or implementation details,
- focuses on **methodology and structure**, rather than deployable performance.

This repository should be viewed as a **methodological demonstration**, not a replication of internal research outputs.

---

## Methodology

### 1. Data & Returns
- Load public asset price data.
- Compute log or simple returns as model inputs.

### 2. Tail-Risk Proxy Construction (Public Demo)
- Construct transparent downside-risk measures, such as:
  - rolling historical CVaR (e.g., 5% tail),
  - maximum drawdown,
  - realized volatility.
- These proxies serve as **public substitutes** for proprietary tail-risk features.

### 3. HMM Regime Inference
- Fit a Hidden Markov Model on observable features (returns and/or tail-risk proxies).
- Infer latent regimes and regime probabilities over time.

### 4. Regime Diagnostics
- Analyze regime transition matrices and state persistence.
- Compare regime-conditioned risk characteristics (e.g., CVaR and volatility by regime).
- Visualize regime segmentation over time.

### 5. Portfolio Construction (Demonstration)
- Construct a **mean–variance optimized (MVO)** portfolio using regime-aware risk estimates.
- This step is included for **illustrative purposes only** to demonstrate how regime information can inform allocation.

---

## Important Note on Backtesting & Look-Ahead Bias
All results reported in this notebook are **in-sample demonstration results**.

Regime inference (HMM), tail-risk estimation, and portfolio optimization are performed using the **same historical window**.  
As a result:

- reported Sharpe ratios and performance metrics may be **inflated**,
- results should **not** be interpreted as out-of-sample or deployable performance,
- the focus is on **workflow structure and modeling logic**, not performance claims.

This design choice is intentional and appropriate for a **public demo notebook**.

---

