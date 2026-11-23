# 🛒 E-Commerce Sales Analytics — End-to-End Data Science Pipeline

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Wrangling-150458?logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/scikit--learn-Modeling-F7931E?logo=scikitlearn&logoColor=white" alt="scikit-learn">
  <img src="https://img.shields.io/badge/XGBoost-Boosting-189AB4" alt="XGBoost">
  <img src="https://img.shields.io/badge/SHAP-Interpretability-8A2BE2" alt="SHAP">
  <img src="https://img.shields.io/badge/Status-Complete-brightgreen" alt="Status">
  <img src="https://img.shields.io/badge/License-MIT-yellow" alt="License">
</p>

<p align="center">
  A full data science workflow on 2022–2024 e-commerce transactions — from feature engineering and
  statistical testing to time series forecasting, profit prediction, and SHAP-driven business
  recommendations.
</p>

---

## 📖 Overview

This project uses a transaction-level e-commerce dataset (2022–2024) to answer a practical question:
**what drives profitability, and how can the business act on it?**

The notebook covers:

- 🧹 **Feature engineering** — cleaning, date features, unit price and profit margin
- 🔍 **EDA** — distributions, category and regional patterns, association rules
- 🧪 **Statistical inference** — normality, variance, ANOVA, post-hoc tests, power analysis
- 📈 **Forecasting** — ARIMA vs. Holt-Winters
- 🤖 **Machine learning** — regularized regression and tree-based ensembles predicting profit
- 💡 **Interpretability** — SHAP and PDP to turn model behavior into business actions

---

## 🗂️ Dataset

| Detail | Description |
|---|---|
| **Source** | <your source / Kaggle link> |
| **File** | `<filename>.csv` |
| **Period** | 2022 – 2024 |
| **Size** | <rows × columns> |
| **Target** | Transaction profit |
| **Key columns** | `Quantity`, `Unit_Price`, `Profit_Margin`, `Category`, `Region`, order date |

> 📥 The raw data is not included in this repo. Place the file in the working directory before running
> the notebook.

---

## 🗺️ Project Structure

```
├── 01. Data Preprocessing & Feature Engineering
├── 02. Exploratory Data Analysis (EDA)
├── 03. Statistical Inference & Experimental Design
├── 04. Time Series Forecasting (ARIMA vs. Holt-Winters)
├── 05. Supervised Machine Learning & Regularized Regressions
└── 06. Interpretability & Strategic Action Items (SHAP/PDP)
```

---

## 🧹 Feature Engineering & Quality Control

1. **Cleaned transactional inconsistencies** and standardized currency formats
2. **Converted date columns** to datetime objects
3. **Extracted time features:** `Year`, `Month`, `Quarter`, `Day of Week`, `Is_Weekend`
4. **Created secondary features:** `Unit_Price` and `Profit_Margin`

---

## 🧪 Statistical Framework

| Test | Purpose | Outcome |
|---|---|---|
| **Shapiro-Wilk + Q-Q plots** | Normality of financial variables | Positive skew confirmed |
| **Levene's test** | Equality of variance across regions | <result> |
| **One-way ANOVA** | Profit differences across product categories | Significant (p < 0.05) |
| **Bonferroni post-hoc** | Which category pairs differ | <result> |
| **Power analysis** | Minimum sample size for future tests | Power = 0.80, α = 0.05 |

---

## 📈 Time Series Forecasting

- Decomposed trend and seasonality with classical additive decomposition and checked stationarity
- Compared **ARIMA (2,1,2)** against **Holt-Winters** exponential smoothing (additive weekly seasonality)
- **Winner:** Holt-Winters, with the lowest MAPE (< 15%)

---

## 🤖 Machine Learning

- Scaled numeric features and encoded high-cardinality categoricals
- Compared linear regression, **Ridge**, **Lasso**, **Random Forest**, **Gradient Boosting**, and **XGBoost**
- **Winner:** XGBoost / Gradient Boosting ensemble

| Model track | Metric | Result |
|---|---|---|
| **Ensemble (test set)** | R² | **≈ 0.89** |
| **Ensemble (test set)** | MAE / MAPE | **$145.67 / 11.56%** |
| **Holt-Winters** | Forecast MAPE | **< 15%** |

### Interpretability
SHAP (global and local) and partial dependence plots identified **Quantity** and **Unit Price** as the
dominant drivers of transaction profit.

---

## 💡 Business Recommendations

1. **Focus on high-margin categories** — direct marketing toward Electronics and premium Office segments
2. **Promote volume bundles** — Quantity is the top profit driver, so use bulk-pricing discounts
3. **Fix negative-margin transactions** — about 10% of transactions lose money; review shipping costs
   and consider regional minimum order values

---

## 🛠️ Tech Stack

- **Data wrangling** — pandas, numpy
- **Statistics** — scipy.stats, statsmodels (power analysis, ACF/PACF)
- **Time series** — statsmodels.tsa (ARIMA, decomposition, Holt-Winters)
- **Machine learning** — scikit-learn, xgboost
- **Interpretability** — shap
- **Association mining** — mlxtend (Apriori)
- **Visualization** — matplotlib, seaborn, networkx, squarify
- **Environment** — Google Colab / Jupyter

---

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/jaminjuma/<repo-name>.git
cd <repo-name>

# Install dependencies
pip install pandas numpy scipy statsmodels scikit-learn xgboost shap mlxtend \
            matplotlib seaborn networkx squarify

# Place the dataset in the project folder, then run the notebook
jupyter notebook
```

---

## 🔮 Possible Next Steps

- Hyperparameter tuning and cross-validation for the final ensemble
- Add prediction intervals to the Holt-Winters forecasts
- Customer segmentation (RFM) and lifetime value modeling
- Deploy the profit model as an API or dashboard

---

## 👤 Author

**Jamin Juma**
Founder of [Automateke](https://automateke.app) · CS student, Kirinyaga University

- 🌐 Portfolio: [jaminjuma.tech](https://jaminjuma.tech)
- 💻 GitHub: [@jaminjuma](https://github.com/jaminjuma)
- 🔗 LinkedIn: [jumajamin](https://linkedin.com/in/jumajamin)

---

## 📄 License

This project is licensed under the MIT License — feel free to use and adapt it.
