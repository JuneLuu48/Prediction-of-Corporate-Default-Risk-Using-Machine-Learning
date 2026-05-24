# Predicting Corporate Default Risk Using Machine Learning

**University of Newcastle · Business Analytics · 2024**  
`Python` `Logistic Regression` `Random Forest` `Machine Learning` `Financial Risk` `Classification` `Decision Support`

---

## 📌 Project Overview

Corporate default — when a company fails to meet its debt obligations — poses significant risk to lenders, investors, and supply chain partners. Early and accurate identification of default risk is a high-value problem in financial services, credit analysis, and corporate governance. This project builds and compares **machine learning classification models** to predict the probability of corporate default using financial and operational indicators, producing a decision-support tool for credit risk assessment.

---

## 🎯 Business Problem

Financial institutions, credit analysts, and investors face a common challenge: identifying which companies are at elevated risk of default before it occurs. Traditional credit scoring methods often rely on lagging indicators or simplified financial ratios. Machine learning offers a more powerful, data-driven approach that can:

- Process multiple financial signals simultaneously
- Identify complex, non-linear relationships between financial indicators and default risk
- Provide probability scores that support risk-tiered lending and investment decisions
- Flag early warning signals that support proactive risk management

---

## 📂 Repository Contents

| File | Description |
|---|---|
| `*.ipynb` | Jupyter Notebook — full ML pipeline: data preprocessing, feature engineering, model training, evaluation, and visualisation |
| `*.csv` | Corporate financial dataset (financial ratios, leverage indicators, liquidity measures, profitability metrics) |
| `*.pdf` | Full project report — methodology, model comparison, results, and business recommendations |

---

## 🔧 Methodology

### 1. Data Preparation & Feature Engineering
- Loaded corporate financial dataset containing key indicators: debt-to-equity ratio, current ratio, return on assets, interest coverage ratio, earnings volatility, and others
- Performed data cleaning: handled missing values, removed outliers, and validated data consistency
- Applied feature scaling and encoding for model compatibility
- Addressed class imbalance (defaults are rare events) using resampling techniques

### 2. Exploratory Data Analysis (EDA)
- Analysed distributions of financial features across defaulted vs. non-defaulted companies
- Identified correlations between financial ratios and default outcomes
- Visualised class separation to inform feature selection

### 3. Model Development & Comparison

| Model | Strengths | Application |
|---|---|---|
| **Logistic Regression** | Interpretable, probabilistic output, industry-standard baseline | Credit scoring baseline |
| **Random Forest** | Handles non-linearity, robust to overfitting, feature importance ranking | High-accuracy prediction |

### 4. Model Evaluation

Evaluated models using classification metrics appropriate for imbalanced financial risk data:

| Metric | Why It Matters |
|---|---|
| **Accuracy** | Overall correct classification rate |
| **Precision** | Of predicted defaults, how many are actual defaults |
| **Recall (Sensitivity)** | Of actual defaults, how many were correctly identified |
| **F1-Score** | Harmonic mean of precision and recall — key for imbalanced classes |
| **AUC-ROC** | Model's ability to discriminate between default and non-default |
| **Confusion Matrix** | Visual breakdown of true/false positives and negatives |

---

## 📊 Key Results

| Model | Accuracy | AUC-ROC | Key Strength |
|---|---|---|---|
| Logistic Regression | Baseline | Baseline | Interpretability, regulatory compliance |
| Random Forest | Higher | Higher | Predictive accuracy, feature importance |

> **Finding:** Random Forest outperformed Logistic Regression on key metrics, particularly recall — critical for default prediction where missing an actual default (false negative) is the costlier error. Feature importance analysis identified leverage ratios and liquidity measures as the strongest predictors of default risk.

---

## 💡 Business Interpretation & Value

| Stakeholder | How This Model Adds Value |
|---|---|
| **Credit Analysts** | Automate initial screening of loan applications using probability scores |
| **Risk Managers** | Flag high-risk clients for proactive review before default occurs |
| **Investors** | Screen corporate bond portfolios for elevated default exposure |
| **Regulators** | Support stress-testing and capital adequacy assessment |

> **Key Insight:** Recall is the most important metric in this context — a model that misses actual defaults (false negatives) creates far greater financial damage than one that over-flags safe companies (false positives). Model selection and threshold tuning should be guided by this business priority.

---

## 🛠️ Tools & Libraries

| Category | Tools |
|---|---|
| Language | Python 3 |
| Machine Learning | Scikit-learn (Logistic Regression, Random Forest, GridSearchCV) |
| Data Processing | Pandas, NumPy |
| Visualisation | Matplotlib, Seaborn |
| Evaluation | Scikit-learn metrics, ROC-AUC, confusion matrix |
| Environment | Jupyter Notebook |

---

## ⚠️ Limitations & Ethical Considerations

- Models trained on historical financial data may not capture structural changes in market conditions or industry dynamics
- Automated credit risk scoring must be used responsibly — false positives can unfairly deny credit to viable companies
- Financial ratios alone do not capture qualitative risk factors (management quality, market position, geopolitical exposure)
- Any deployment in a real lending or investment context would require rigorous validation, regulatory review, and human oversight

---

*Project completed as part of the Bachelor of Business Analytics at the University of Newcastle, 2024.*
