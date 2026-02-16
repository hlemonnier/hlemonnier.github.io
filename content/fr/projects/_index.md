---
title: "Projets"
description: "Case studies de recherche quantitative et de strategies systematiques."
filters: ["Python", "RL", "Market Making", "Risk", "ML"]
caseStudies:
  - title: "Pipeline alpha microstructure court horizon"
    period: "2025 - Enigma Securities"
    summary: "Pipeline predictif orienté execution pour des signaux de marche court horizon."
    problem: "Construire des signaux intraday robustes a partir de microstructure bruitee tout en preservant la qualite out-of-sample."
    method:
      - "Engineering d'un large set de features (order-flow, liquidite, volatilite, derives)."
      - "Construction d'un workflow reproductible research-to-production (pipeline de features, entrainement, validation, reporting, monitoring hooks)."
      - "Validation robuste via walk-forward splits, diagnostics de regime et etudes d'ablation."
    results:
      - "Signal out-of-sample statistiquement significatif sur horizons courts."
      - "Cycles de recherche accelérés grace a l'automatisation experimentation/reporting."
      - "Meilleure tracabilite des signaux pour les regles de decision d'execution."
    stack: ["Python", "Pandas", "NumPy", "Scikit-learn", "ML", "Risk"]
    tags: ["ML", "Risk"]
    github: "https://github.com/hlemonnier"

  - title: "Market making adaptatif (Avellaneda-Stoikov + SAC RL)"
    period: "2025 - Enigma Securities"
    summary: "Cadre d'execution combinant controle inventory-aware et adaptation par reinforcement learning."
    problem: "Maintenir la performance market-making quand les regimes microstructure changent, tout en controlant inventory et adverse selection."
    method:
      - "Implementation d'un baseline Avellaneda-Stoikov event-driven avec skew inventory-aware et controle spread/refresh."
      - "Conception de signaux microstructure pour limiter l'adverse selection (order-flow imbalance, liquidity imbalance, proxies de queue)."
      - "Prototype SAC pour ajuster dynamiquement les parametres de cotation."
    results:
      - "Amelioration out-of-sample des rendements ajustes du risque a intensite d'execution comparable."
      - "Adaptation plus rapide aux regimes de marche qu'un parametrage statique."
      - "Execution plus reguliere sur les metriques de qualite en backtest."
    stack: ["Python", "RL", "Market Making", "Risk", "PyTorch"]
    tags: ["RL", "Market Making", "Risk"]
    github: "https://github.com/hlemonnier"

  - title: "Optimisation de portefeuille et strategie BTC TSM multi-horizons"
    period: "Recherche personnelle"
    summary: "Deux axes: frontiere efficiente Monte Carlo et modele trend BTC long-only."
    problem: "Construire des frameworks d'allocation et de trend interpretables avec un controle explicite du risque baissier."
    method:
      - "Developpement d'un optimiseur Monte Carlo en Python pour generer des frontieres efficientes sur des milliers de vecteurs de poids."
      - "Conception d'un signal trend BTC long-only base sur PCA 120 jours + lissage EMA."
      - "Mise en place d'un ciblage de volatilite baissiere (90%) avec levier max de 2x."
    results:
      - "Cartographie stable des compromis rendement/risque pour l'allocation."
      - "Meilleur controle du drawdown sur regimes BTC volatils."
      - "Composants de recherche reutilisables pour signaux et overlays de risque."
    stack: ["Python", "ML", "Risk", "Pandas", "NumPy"]
    tags: ["Python", "ML"]
    github: "https://github.com/hlemonnier"
---
