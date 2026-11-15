# BCG X Data Science Job Simulation
### Forage · PowerCo Customer Churn Prediction

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat-square&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Random%20Forest-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-22c55e?style=flat-square)
![Forage](https://img.shields.io/badge/Forage-BCG%20X-FF6B35?style=flat-square)

---

## Overview

This repository contains my completed work for the **BCG X Data Science Job Simulation** hosted on [Forage](https://www.theforage.com/). The simulation mirrors a real-world consulting engagement where BCG X is hired by **PowerCo** — a major gas and electricity utility — to investigate and reduce customer churn.

**Core hypothesis:** Price sensitivity is a primary driver of churn, and a 20% discount could serve as a viable retention lever.

>  **Client:** PowerCo (fictitious utility company)  
>  **Simulated Role:** Data Scientist @ BCG X  
>  **Goal:** Predict churn, identify its drivers, and evaluate the financial case for a targeted discount strategy

---

## 🗂️ Simulation Tasks

### Task 1 — Business Understanding & Hypothesis Framing
- Analyzed the client brief and decomposed the churn problem from a business perspective
- Identified the key question: *Is price the main reason customers are leaving?*
- Drafted a structured email to the Associate Director outlining the data needed and the analytical approach to test the hypothesis

### Task 2 — Exploratory Data Analysis
- Explored `client_data.csv` and `price_data.csv` for data quality, distributions, and anomalies
- Investigated churn rates across segments — contract types, consumption levels, and regions
- Generated visualizations (stacked bar charts, histograms, correlation heatmaps) to surface patterns
- Output: `clean_data_after_eda.csv` — cleaned and validated dataset ready for feature engineering

### Task 3 — Feature Engineering &nbsp;·&nbsp; [`Task-3.ipynb`](./Task-3.ipynb)
- Engineered price-sensitivity features: max price delta and average price change across off-peak, peak, and mid-peak periods
- Applied log transformation to skewed numerical features (consumption, forecast columns)
- Encoded categorical variables and resolved missing values
- Output: `data_for_predictions.csv` — fully engineered feature set

### Task 4 — Predictive Modelling &nbsp;·&nbsp; [`Task-4.ipynb`](./Task-4.ipynb)
- Trained a **Random Forest Classifier** to predict customer churn probability
- Evaluated using accuracy, precision, recall, F1-score, and confusion matrix
- Extracted and ranked feature importances to understand what actually drives churn

### Task 5 — Model Evaluation & Insights &nbsp;·&nbsp; [`Task-5.ipynb`](./Task-5.ipynb)
- Fine-tuned model hyperparameters for better generalization
- Assessed the business viability of the 20% discount: modelled expected revenue saved vs. discount cost across predicted churners
- Key finding: **price sensitivity is a mid-tier predictor** — net margin and 12-month consumption patterns are stronger churn signals

### Task 6 — Executive Summary &nbsp;·&nbsp; [`EXECUTIVE SUMMARY.pdf`](./EXECUTIVE%20SUMMARY.pdf)
- Synthesized all findings into a concise, executive-ready PDF
- Communicated model results, top churn drivers, and a clear recommendation on the discount strategy
- Advised a **targeted** discount approach (high-value, high-risk customers only) over a blanket rollout

---

## 📁 Repository Structure

```
BCGX/
│
├── client_data.csv               # Raw customer data (usage, contracts, demographics)
├── price_data.csv                # Historical electricity pricing by time period
│
├── clean_data_after_eda.csv      # Cleaned dataset produced after EDA (Task 2)
├── data_for_predictions.csv      # Feature-engineered dataset for modelling (Task 3)
│
├── Task-3.ipynb                  # Feature Engineering
├── Task-4.ipynb                  # Random Forest Model Training & Evaluation
├── Task-5.ipynb                  # Model Refinement & Business Insights
│
├── EXECUTIVE SUMMARY.pdf         # Final findings & recommendations (Task 6)
└── README.md
```


---

## Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3.10+ |
| Data Manipulation | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | scikit-learn — Random Forest, metrics, preprocessing |
| Environment | Jupyter Notebook |
| Version Control | Git & GitHub |

---

##  Key Results

| Metric | Value |
|---|---|
| Model | Random Forest Classifier |
| Top Churn Predictors | Net margin, 12-month consumption, tenure |
| Price Sensitivity Rank | Mid-tier (not the primary driver) |
| Discount Strategy Verdict | Viable only for targeted high-risk segment |

---

##  Getting Started

```bash
# 1. Clone the repository
https://github.com/Just-Aditya/BCGX.git
cd BCGX

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# 3. Launch Jupyter and open notebooks in order
jupyter notebook
```

Open in sequence: `Task-3.ipynb` → `Task-4.ipynb` → `Task-5.ipynb`

---