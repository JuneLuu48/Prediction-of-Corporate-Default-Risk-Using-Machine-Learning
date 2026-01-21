# Prediction of Corporate Default Risk Using Machine Learning

## Project Overview
This project predicts the probability of firm default using financial and firm-level variables. The main model is a Decision Tree, compared with Logistic Regression, Random Forest, and Support Vector Classifier (SVC) for performance benchmarking. The goal is to identify key financial and non-financial factors affecting default risk and provide interpretable insights for decision-making.

## Dataset
### Observations: 100,000 simulated firm-level records
### Target: Default (0) / No Default (1)
### Variables:
* Financial Ratios: Debt-to-Asset Ratio, Current Ratio, Return on Assets (ROA), Cash Flow to Debt, Firm Size
* Non-Financial: ESG Score, Industry
* Reason for simulation: Confidentiality, data availability, and controlled variable ranges

## Methodology
Decision Tree: Interpretable tree-based model using if-then rules
Random Forest: Ensemble of trees to reduce overfitting and capture nonlinear patterns
Logistic Regression: Stable, interpretable model using sigmoid function
SVC: Captures complex decision boundaries using kernel functions

## Key Features & Economic Justification
* Debt-to-Asset Ratio	Higher → increases risk	Measures firm leverage
* Current Ratio	Higher → decreases risk	Reflects liquidity; nonlinear effect
* ROA	Higher → decreases risk	Indicates profitability efficiency
* Firm Size	Larger → decreases risk	Diversification and financing access
* Cash Flow to Debt	Higher → decreases risk	Solvency indicator
* ESG Score	Higher (weaker) → slightly increases risk	Reflects sustainability performance
* Industry	Sector-specific	Manufacturing/Construction reduce risk more than Services

## Results
### Decision Tree (tuned):
* Accuracy: 91%
* Precision: 91–92%
* Recall: 91–92%
### Comparison:
* Logistic Regression: 92%
* Random Forest: 91.5%
* SVC: 92%

## Limitations
* Risk of overfitting due to correlated variables
* Simulated data lacks real-world variability
* Limited macroeconomic indicators (e.g., GDP, recession effects)

## Recommendations
* Include macroeconomic factors to capture systemic risk
* Use ensemble learning (e.g., Gradient Boosting) for improved stability
* Incorporate ESG ratings and real-time transaction data for dynamic solvency monitoring

