# car-price-ml-prediction
ML models to predict used car prices using vehicle data + economic indicators from 2014 - 2015

## Overview
This project was completed as a final project for CIS 545 (Big Data Analytics). We integrated 9+ datasets to build and compare multiple regression models.

## Data Sources
- **Vehicle Sales Data** (Kaggle) — ~440K rows of individual car sales (2014–2015)
- Zillow housing prices, US population data, EIA gas prices, Google Trends, NAIC insurance data, and more

## Methods
- **EDA** — geographic visualizations, correlation analysis, time-series exploration
- **Unsupervised Learning** — PCA, t-SNE
- **Linear Models** — OLS, Elastic Net (Lasso), Forward Stepwise Selection
- **Non-Linear Models** — Random Forest, XGBoost
- **Deep Learning** — PyTorch neural network

## Results

| Model | R² | RMSE |
|---|---|---|
| OLS Regression | 0.669 | ~$4,750 |
| Elastic Net | 0.673 | $4,757 |
| Random Forest | 0.722 | $4,389 |
| Deep Learning | 0.760 | ~$4,000 |
| **XGBoost** | **0.866** | **$3,052** |

**Key finding:** Car age and odometer reading are the strongest predictors of price. Brand tier (luxury vs. mainstream) and body style (cab/SUV) drive the largest premiums. Macro-economic and color features have minimal impact.

## Setup
1. Clone the repo
2. Add your `kaggle.json` API token to `~/.kaggle/`
3. Run cells in order in Google Colab or Jupyter

## Tech Stack
`Python` · `pandas` · `scikit-learn` · `XGBoost` · `PyTorch` · `Plotly` · `Seaborn`
