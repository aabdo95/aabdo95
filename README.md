<div align="center">

# Abdelrahman Ahmed

**ML systems · market microstructure · quantitative research**

[![LinkedIn](https://img.shields.io/badge/linkedin-abdelaahmed-b45309?style=flat-square&labelColor=1c1917&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abdelaahmed/)
[![Email](https://img.shields.io/badge/email-hafez__123-b45309?style=flat-square&labelColor=1c1917&logo=maildotru&logoColor=white)](mailto:hafez_123@outlook.com)
[![Available](https://img.shields.io/badge/available-june%202027-1c1917?style=flat-square&labelColor=1c1917)](https://www.linkedin.com/in/abdelaahmed/)

</div>

```
READING · ABDELRAHMAN AHMED                                    ● FINAL YEAR

  EDUCATION    BSc Computer Science, University of Leeds
               First Class · 10% merit scholarship · graduating Jun 2027
  FOCUS        ML engineering / quantitative research — indifferent, taking the best fit
  PREVIOUSLY   Al Wathba National Insurance · KPMG Lower Gulf
  LANGUAGES    Arabic, English
```

I build machine-learning systems and hold them to the standard of evidence they'd
face on a trading desk: no leakage, real costs, and the limitations published
alongside the results.

---

## signal-infra

**[github.com/aabdo95/signal-infra](https://github.com/aabdo95/signal-infra)** — real-time ML signal pipeline on live Kraken data, evaluated by out-of-sample paper trading

```
   kraken v2 websocket
          │              order book rebuilt, CRC32-verified every frame
          ▼              exponential backoff, gap backfill on reconnect
     ingestion ─────────▶ timescaledb ◀───────── redis
          │                    │
          │                    ▼
          │             feature engine          13 microstructure features
          │                    │                forward-only · one code path
          │                    ▼                for both live and replay
          │                lightgbm             purged k-fold CV + embargo
          │                    │                OOS boundary enforced ×3
          │                    ▼
          └───────────▶  paper trader           real taker fees + slippage floor
                               │                append-only track record
                   ┌───────────┴───────────┐
                   ▼                       ▼
              monitoring               dashboard
         PSI drift · two-sided      deflated sharpe flagged
         z-score · human-gated      over raw · methodology
         model promotion            and limitations pages
```

Look-ahead bias is impossible by construction rather than by discipline. One
forward-only engine feeds both the live and the replay path, and the leakage tests
carry a deliberately planted future-peeking feature, so a green test run can never be
an empty one. The out-of-sample boundary is locked in three independent places — an
in-sample row is physically unstorable, not merely discouraged.

Every simulated trade is charged real taker fees and a slippage floor, and the
deflated Sharpe is reported beside the raw one. On a record this short, a large edge
is a bug worth hunting, not a result worth selling.

```
161 tests   ~79% coverage   6 services   mypy --strict + import-linter on every push
```

<sub>
<img src="https://img.shields.io/badge/python-b45309?style=flat-square&labelColor=1c1917&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/lightgbm-b45309?style=flat-square&labelColor=1c1917" />
<img src="https://img.shields.io/badge/mlflow-b45309?style=flat-square&labelColor=1c1917&logo=mlflow&logoColor=white" />
<img src="https://img.shields.io/badge/timescaledb-b45309?style=flat-square&labelColor=1c1917&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/redis-b45309?style=flat-square&labelColor=1c1917&logo=redis&logoColor=white" />
<img src="https://img.shields.io/badge/fastapi-b45309?style=flat-square&labelColor=1c1917&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/docker-b45309?style=flat-square&labelColor=1c1917&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/react-b45309?style=flat-square&labelColor=1c1917&logo=react&logoColor=white" />
</sub>

---

## FIFA World Cup 2026 Predictor

**[wc26-predictor.vercel.app](https://wc26-predictor-abdelrahman-s-projects95.vercel.app/)** — calibrated forecasting across the full 48-team tournament

A Dixon–Coles Poisson model blended with a gradient-boosted ensemble — XGBoost,
LightGBM, CatBoost and logistic regression — trained on more than 47,000
international matches and 49 engineered features. Blend weights tuned by maximum
likelihood on past tournaments, with isotonic calibration and chronological splits so
nothing leaked in from the future. 50,000 Monte Carlo runs produce group standings,
knockout odds and per-match SHAP explanations.

Published before a ball was kicked, with Spain at 24.8%. The model called the top
four, and the champion.

```
0.881 log loss   60.1% accuracy   50,000 simulations   49 features   72 matches
```

<sub>
<img src="https://img.shields.io/badge/python-b45309?style=flat-square&labelColor=1c1917&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/xgboost-b45309?style=flat-square&labelColor=1c1917" />
<img src="https://img.shields.io/badge/catboost-b45309?style=flat-square&labelColor=1c1917" />
<img src="https://img.shields.io/badge/shap-b45309?style=flat-square&labelColor=1c1917" />
<img src="https://img.shields.io/badge/scikit--learn-b45309?style=flat-square&labelColor=1c1917&logo=scikitlearn&logoColor=white" />
<img src="https://img.shields.io/badge/react-b45309?style=flat-square&labelColor=1c1917&logo=react&logoColor=white" />
</sub>

---

## Flight Booking System

**[github.com/aabdo95/COMP2850-Final-Project](https://github.com/aabdo95/COMP2850-Final-Project)** — full-stack booking app built with an Agile team

Front end plus a management dashboard tracking simulated flight metrics across 350+
routes.

<sub>
<img src="https://img.shields.io/badge/javascript-b45309?style=flat-square&labelColor=1c1917&logo=javascript&logoColor=white" />
<img src="https://img.shields.io/badge/sql-b45309?style=flat-square&labelColor=1c1917&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/html%2Fcss-b45309?style=flat-square&labelColor=1c1917&logo=html5&logoColor=white" />
</sub>

---

## Stack

```
LANGUAGES   python · c · typescript/javascript · sql · kotlin · bash
ML          lightgbm · xgboost · catboost · scikit-learn · pytorch · shap · optuna · mlflow
DATA        polars · pandas · numpy · scipy · postgresql · timescaledb · redis
SYSTEMS     docker · github actions · fastapi · react · websockets · aws · azure · linux
```

---

## Experience

| | | |
|---|---|---|
| **2026** | IT Intern | **Al Wathba National Insurance** — reported to the Head of IT at a listed insurer, across application development, cloud infrastructure and information security. Assessed the firm's security posture against the OWASP Top 10 and MITRE ATT&CK, mapped exposures to PDPL, NESA and ADHICS, and presented findings to management. |
| **2025–26** | Level 2 Student Mentor | **University of Leeds** — mentored Level 1 students through a robotics project, ran their code reviews, presented final solutions to faculty. |
| **2024–25** | Course Representative | **University of Leeds** — elected to speak for 300+ students; worked with faculty on data-driven changes to course structure. |
| **2024** | IT Audit Intern | **KPMG Lower Gulf** — validated 1,054 controls across systems underpinning AED 440M of annual revenue, identified 12 critical control weaknesses, led GITC testing across 6 ERP and legacy systems, cut evidence collection time 30% through SQL automation. |
