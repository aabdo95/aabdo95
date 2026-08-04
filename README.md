<div align="center">

# Abdelrahman Ahmed

**ML systems · market microstructure · quantitative research**

[![LinkedIn](https://img.shields.io/badge/linkedin-abdelaahmed-b45309?style=flat-square&labelColor=1c1917&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abdelaahmed/)
[![Email](https://img.shields.io/badge/email-hafez__123-b45309?style=flat-square&labelColor=1c1917&logo=maildotru&logoColor=white)](mailto:hafez_123@outlook.com)


</div>

```
READING · ABDELRAHMAN AHMED                                    ● FINAL YEAR

  EDUCATION    BSc Computer Science, University of Leeds
               First Class · 10% merit scholarship · graduating Jun 2027
  FOCUS        ML/AI engineering, Quantitative development 
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

### Tech Stack

<div align="center">
  
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)
 
![LightGBM](https://img.shields.io/badge/LightGBM-9ACD32?style=for-the-badge&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-EC5A2A?style=for-the-badge&logoColor=white)
![CatBoost](https://img.shields.io/badge/CatBoost-FFCC00?style=for-the-badge&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![SHAP](https://img.shields.io/badge/SHAP-1F77B4?style=for-the-badge&logoColor=white)
![Optuna](https://img.shields.io/badge/Optuna-2C6BAA?style=for-the-badge&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white)
 
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Polars](https://img.shields.io/badge/Polars-CD792C?style=for-the-badge&logo=polars&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![TimescaleDB](https://img.shields.io/badge/TimescaleDB-FDB515?style=for-the-badge&logo=timescale&logoColor=black)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
 
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
 
</div>

---
