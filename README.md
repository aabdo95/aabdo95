<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=140&section=header&text=Abdelrahman%20Ahmed&fontSize=42&fontColor=ffffff&fontAlignY=55&desc=CS%20%40%20University%20of%20Leeds%20·%20AI%2FML%20Engineering%20·%20Quantitative%20Research&descAlignY=78&descSize=15&descColor=a78bfa" />

[![LinkedIn](https://img.shields.io/badge/LinkedIn-abdelaahmed-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abdelaahmed/)
[![Email](https://img.shields.io/badge/Email-Get%20In%20Touch-ea4335?style=for-the-badge&logo=maildotru&logoColor=white)](mailto:hafez_123@outlook.com)

</div>

---

### About

```python
abdelrahman = {
    "education":  "BSc Computer Science @ University of Leeds — First Class, 10% merit scholarship",
    "graduating": "June 2027",
    "experience": ["IT Intern @ Al Wathba National Insurance", "IT Audit Intern @ KPMG Lower Gulf"],
    "building":   "signal-infra — a real-time ML signal pipeline on live market data",
    "interests":  ["Machine Learning", "Quantitative Research", "Market Microstructure"],
    "languages":  ["Arabic (fluent)", "English (fluent)"],
}
```

---

### Selected work

**[signal-infra](https://github.com/aabdo95/signal-infra)** — real-time ML trading signal pipeline
`Python` `LightGBM` `MLflow` `TimescaleDB` `Docker` `React`

A live pipeline on Kraken's WebSocket feed that rebuilds the order book, verifies it against the exchange CRC32 on every frame, and writes to TimescaleDB in single transactions. Look-ahead bias is impossible by construction: one forward-only engine computes 13 microstructure features for both the live and replay paths, and the leakage tests carry a deliberately planted future-peeking feature so a green run can never be an empty one. LightGBM trained under purged k-fold CV with an embargo, with the out-of-sample boundary locked in three independent places. Real taker fees and a slippage floor are charged on every simulated trade, and the deflated Sharpe is reported beside the raw one — on a short record, a large edge is a bug worth hunting, not a result worth selling.

> 161 tests · ~79% coverage · 6 Docker services · strict typing and module boundary contracts on every push

**[FIFA World Cup 2026 Predictor](https://wc26-predictor-abdelrahman-s-projects95.vercel.app/)** — calibrated tournament forecasting
`Python` `XGBoost` `LightGBM` `CatBoost` `SHAP` `FastAPI` `React`

A Dixon–Coles Poisson model blended with a gradient-boosted ensemble, trained on 47,000+ international matches and 49 engineered features. Blend weights tuned by MLE on past tournaments — 0.881 log loss, 60.1% accuracy, isotonic calibration, chronological splits. 50,000 Monte Carlo runs of the 48-team tournament produce group standings, knockout odds and per-match SHAP explanations. Published before the tournament with Spain at 24.8%; the model called the top four, and the champion.

**[Flight Booking System](https://github.com/aabdo95/COMP2850-Final-Project)** — full-stack booking app
`JavaScript` `SQL` `HTML/CSS`

Built with an Agile team: front end plus a management dashboard tracking simulated flight metrics across 350+ routes.

---

### Tech stack

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)

![LightGBM](https://img.shields.io/badge/LightGBM-02569B?style=for-the-badge&logo=lightning&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-EC5A2A?style=for-the-badge&logo=xgboost&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white)
![Polars](https://img.shields.io/badge/Polars-CD792C?style=for-the-badge&logo=polars&logoColor=white)

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/TimescaleDB-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

</div>

---

### Experience

| Role | Organisation | What I did |
|------|--------------|------------|
| IT Intern | Al Wathba National Insurance | Reported to the Head of IT at a listed insurer, across application development, cloud infrastructure and information security. Assessed the firm's security posture against the OWASP Top 10 and MITRE ATT&CK, mapped exposures to PDPL, NESA and ADHICS, and presented findings to management. |
| IT Audit Intern | KPMG Lower Gulf | Validated 1,054 controls across systems underpinning AED 440M of annual revenue · identified 12 critical control weaknesses · led GITC testing across 6 ERP and legacy systems · cut evidence collection time 30% through SQL automation. |
| Course Representative | University of Leeds | Elected to speak for 300+ students; worked with faculty on data-driven changes to course structure. |
| Level 2 Student Mentor | University of Leeds | Mentored Level 1 students through a robotics project, ran code reviews, presented final solutions to faculty. |

---

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=100&section=footer" />
</div>
