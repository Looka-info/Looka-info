# Hi, I'm Looka 👋

### AI / Machine Learning Engineer

I build end-to-end machine learning systems: leak-free data pipelines, rigorous evaluation, and production-ready serving. I care about honest metrics, strong baselines, and documenting what doesn't work.

[![Portfolio](https://img.shields.io/badge/Portfolio-mumer.info-0A66C2?style=flat-square&logo=googlechrome&logoColor=white)](https://mumer.info)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-mumerinfo-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mumerinfo/)
[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=flat-square&logo=kaggle&logoColor=white)](https://www.kaggle.com/)

---

## Featured Projects

### 🌿 [PlantVision: Plant Leaf Disease Classifier](https://github.com/Looka-info/Computer-vision-classifier)
`PyTorch` `ResNet-18` `Transfer Learning` `Streamlit`

A scratch CNN compared against a fine-tuned ResNet-18 across 38 disease classes (54,284 images, PlantVillage).

- **99.03%** top-1 accuracy (vs 88.96% for the baseline CNN), **0.9871** macro-F1
- Well calibrated: **ECE 0.0040**; confidence gating gives **99.56%** accuracy at 98.52% coverage
- Data integrity: SHA-256 and perceptual-hash audit found **0** train/test leakage pairs; specimen-isolated validation and test splits
- **~21 ms** warm end-to-end inference; interactive Streamlit demo; 29 automated tests

### 📉 [Customer Churn Prediction](https://github.com/Looka-info/Customer-churn-prediction)
`scikit-learn` `SQL` `Streamlit` `pytest`

Logistic Regression, Random Forest and Gradient Boosting compared on the IBM Telco dataset (7,043 customers, 26.5% churn).

- Leakage-safe preprocessing pipeline; **PR-AUC** as the primary metric for the imbalanced target
- Nadeau–Bengio corrected resampled t-test showed the complex models did not significantly outperform the baseline (p > 0.35)
- Decision thresholds tuned on expected campaign value, with sensitivity analysis across business scenarios
- SQL cross-verification, interactive Streamlit dashboard, 38 automated tests

### 📦 [DemandCast: Production ML Forecasting System](https://github.com/Looka-info/Production-ML-forecasting-system)
`FastAPI` `MLflow` `Docker` `LightGBM` `GitHub Actions`

Weekly demand forecasting across 15,053 product–warehouse series (VN1 benchmark) and UCI Online Retail II.

- Chronological backtesting with 13-week horizons; official VN1 benchmark reproduced
- Versioned model registry with atomic release pointer and rollback
- FastAPI serving with drift, bias and data-freshness monitoring
- Shadow-forecasting pipeline: candidate vs production on identical inputs, with failure isolation
- CI with linting and tests; documented finding that tuned baselines beat LightGBM on validation

---

## Skills

**Machine Learning:** PyTorch · TensorFlow · Keras · scikit-learn · LightGBM · Hugging Face

**Data:** Python · NumPy · Pandas · SciPy · SQL · Matplotlib · Plotly · Jupyter

**MLOps & Serving:** FastAPI · Streamlit · MLflow · Docker · GitHub Actions · pytest · Ruff

**Also:** JavaScript · React · HTML/CSS · C/C++ · Git · Figma

<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" />
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" />
<img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" />
<img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" />
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" />
<img src="https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
<img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
</p>

---

## Engineering Approach

- **No data leakage:** split before preprocessing, deduplicate by hash, enforce point-in-time cutoffs
- **Right metrics:** PR-AUC for imbalance, calibration (ECE) for trust, WAPE and bias for forecasting
- **Statistical rigor:** cross-validation, corrected significance tests, ablation studies
- **Production mindset:** model registry, rollback, monitoring, containerization, CI
- **Honest reporting:** every project documents limitations and what didn't work

---

## GitHub Stats

<p>
  <img height="160" alt="GitHub stats" src="https://github-readme-stats.vercel.app/api?username=looka-info&show_icons=true&hide_border=true&theme=default#gh-light-mode-only" />
  <img height="160" alt="GitHub stats" src="https://github-readme-stats.vercel.app/api?username=looka-info&show_icons=true&hide_border=true&theme=github_dark#gh-dark-mode-only" />
  <img height="160" alt="Top languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=looka-info&layout=compact&hide_border=true&theme=default#gh-light-mode-only" />
  <img height="160" alt="Top languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=looka-info&layout=compact&hide_border=true&theme=github_dark#gh-dark-mode-only" />
</p>

---

## Currently

- Extending PlantVision with a FastAPI + Docker serving layer
- Adding probability calibration and uplift modeling to the churn project
- Learning LLM applications and retrieval-augmented generation (RAG)

## Get in Touch

Open to collaboration and ML engineering opportunities. Reach me via [LinkedIn](https://www.linkedin.com/in/mumerinfo/) or [mumer.info](https://mumer.info).
