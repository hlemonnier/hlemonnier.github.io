---
title: "Projects"
description: "Case studies from my quant research and systematic strategy work."
filters: ["Python", "RL", "Market Making", "Risk", "ML"]
caseStudies:
  - title: "Short-Horizon Microstructure Alpha Pipeline"
    period: "2025 - Enigma Securities"
    summary: "Predictive modeling pipeline for execution-aware short-horizon market signals."
    problem: "How to produce stable, statistically significant intraday signals from noisy market microstructure while preserving out-of-sample robustness."
    method:
      - "Engineered a broad feature set spanning order-flow, liquidity, volatility, and derivatives-based variables."
      - "Built a reproducible research-to-production workflow (feature pipeline, training orchestration, validation, reporting, monitoring hooks)."
      - "Applied walk-forward splits, regime diagnostics, and ablation studies to isolate real signal contribution and reduce overfitting."
    results:
      - "Delivered statistically significant out-of-sample signal quality on short horizons."
      - "Reduced iteration cycles through automated experimentation and reporting."
      - "Improved model traceability for downstream execution decision rules."
    stack: ["Python", "Pandas", "NumPy", "Scikit-learn", "ML", "Risk"]
    tags: ["ML", "Risk"]
    github: "https://github.com/hlemonnier"

  - title: "Adaptive Market Making (Avellaneda-Stoikov + SAC RL)"
    period: "2025 - Enigma Securities"
    summary: "Execution framework combining model-based inventory control with reinforcement learning adaptation."
    problem: "How to maintain market-making performance under changing microstructure regimes while controlling inventory and adverse selection."
    method:
      - "Implemented an event-driven Avellaneda-Stoikov baseline with inventory-aware skew and spread/refresh controls."
      - "Designed microstructure signals for adverse selection control (order-flow imbalance, liquidity imbalance, queue proxies)."
      - "Prototyped a SAC agent to adapt quoting parameters dynamically across market regimes."
    results:
      - "Improved out-of-sample risk-adjusted returns at similar execution intensity."
      - "Increased policy adaptivity versus static parameter baselines."
      - "Improved consistency of execution quality metrics in backtests."
    stack: ["Python", "RL", "Market Making", "Risk", "PyTorch"]
    tags: ["RL", "Market Making", "Risk"]
    github: "https://github.com/hlemonnier"

  - title: "Portfolio Optimization and BTC Multi-Horizon TSM"
    period: "Independent Research"
    summary: "Two strategy research tracks: Monte Carlo efficient frontier optimization and BTC long-only trend modeling."
    problem: "How to build transparent allocation and trend frameworks that remain interpretable while controlling downside risk."
    method:
      - "Built a Python Monte Carlo optimizer to generate efficient frontiers across thousands of portfolio weight vectors."
      - "Developed a BTC long-only trend framework using a 120-day PCA signal with EMA smoothing."
      - "Applied downside volatility targeting (90%) with a leverage cap of 2x."
    results:
      - "Produced stable risk/return trade-off maps for portfolio allocation analysis."
      - "Improved drawdown control under volatile BTC regimes."
      - "Created reusable research components for signal and risk overlays."
    stack: ["Python", "ML", "Risk", "Pandas", "NumPy"]
    tags: ["Python", "ML"]
    github: "https://github.com/hlemonnier"
---
