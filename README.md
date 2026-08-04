# Abdelrahman Ahmed

BSc Computer Science, University of Leeds — First Class, graduating June 2027.
Looking for graduate roles in AI/ML engineering or quantitative research.

I build machine-learning systems and hold them to the standard of evidence they'd
face on a trading desk: no leakage, real costs, and the limitations published
alongside the results.

[LinkedIn](https://www.linkedin.com/in/abdelaahmed/) · [hafez_123@outlook.com](mailto:hafez_123@outlook.com)

---

## Selected work

### [signal-infra](https://github.com/aabdo95/signal-infra)

Real-time ML signal pipeline on live Kraken market data, evaluated by out-of-sample
paper trading.

The pipeline rebuilds the order book from the WebSocket feed, verifies it against the
exchange CRC32 on every frame, and writes to TimescaleDB in single transactions — it
rode out a forced database restart mid-run with no gaps and no duplicate rows.

Look-ahead bias is impossible by construction rather than by discipline: one
forward-only engine computes 13 microstructure features for both the live and the
replay path, and the leakage tests carry a deliberately planted future-peeking
feature, so a green test run can never be an empty one. A LightGBM classifier is
trained under purged k-fold cross-validation with an embargo, versioned in MLflow,
with the out-of-sample boundary locked in three independent places — an in-sample row
is physically unstorable, not merely discouraged.

Every simulated trade is charged real taker fees and a slippage floor, and the
deflated Sharpe is reported beside the raw one. On a record this short, a large edge
is a bug worth hunting, not a result worth selling.

`Python` `LightGBM` `MLflow` `TimescaleDB` `Redis` `FastAPI` `Docker` `React`

    161 tests · ~79% coverage · 6 services · mypy --strict and import-linter on every push

### [FIFA World Cup 2026 Predictor](https://wc26-predictor-abdelrahman-s-projects95.vercel.app/)

A Dixon–Coles Poisson model blended with a gradient-boosted ensemble — XGBoost,
LightGBM, CatBoost and logistic regression — trained on more than 47,000
international matches and 49 engineered features. Blend weights tuned by maximum
likelihood on past tournaments, with isotonic calibration and chronological splits so
nothing leaked in from the future. 50,000 Monte Carlo runs of the 48-team tournament
produce group standings, knockout odds and per-match SHAP explanations.

Published before a ball was kicked, with Spain at 24.8%. The model called the top
four, and the champion.

`Python` `XGBoost` `LightGBM` `CatBoost` `SHAP` `FastAPI` `React`

    0.881 log loss · 60.1% accuracy · 50,000 simulations · 72 matches

### [Flight Booking System](https://github.com/aabdo95/COMP2850-Final-Project)

Full-stack booking application built with an Agile team: front end plus a management
dashboard tracking simulated flight metrics across 350+ routes.

`JavaScript` `SQL` `HTML/CSS`

---

## Stack

    Languages     Python · C · TypeScript/JavaScript · SQL · Kotlin · Bash
    ML            LightGBM · XGBoost · CatBoost · scikit-learn · PyTorch · SHAP · Optuna · MLflow
    Data          Polars · Pandas · NumPy · SciPy · PostgreSQL · TimescaleDB · Redis
    Systems       Docker · GitHub Actions · FastAPI · React · WebSockets · AWS · Azure · Linux

---

## Experience

| | | |
|---|---|---|
| **2026** | IT Intern | **Al Wathba National Insurance** — reported to the Head of IT at a listed insurer, across application development, cloud infrastructure and information security. Assessed the firm's security posture against the OWASP Top 10 and MITRE ATT&CK, mapped exposures to PDPL, NESA and ADHICS, and presented findings to management. |
| **2025–26** | Level 2 Student Mentor | **University of Leeds** — mentored Level 1 students through a robotics project, ran their code reviews, presented final solutions to faculty. |
| **2024–25** | Course Representative | **University of Leeds** — elected to speak for 300+ students; worked with faculty on data-driven changes to course structure. |
| **2024** | IT Audit Intern | **KPMG Lower Gulf** — validated 1,054 controls across systems underpinning AED 440M of annual revenue, identified 12 critical control weaknesses, led GITC testing across 6 ERP and legacy systems, cut evidence collection time 30% through SQL automation. |
