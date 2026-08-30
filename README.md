# AI Agent / Capstone Project: Predicting Search Ranking Shifts

> **Abstract:** This project delivers an automated machine learning and data processing pipeline designed to forecast search engine ranking shifts, providing actionable decision support for digital growth and SEO optimization.

## 1. What it does and for whom
* **Functionality:** Ingests SERP and content feature matrices, applies feature engineering, and runs a gradient-boosted regression pipeline to predict 14-day search ranking fluctuations.
* **Target Audience:** Content strategists, SEO engineers, and data science teams looking to prioritize technical optimizations before traffic drops occur.

## 2. Setup (Stranger-Reproducible)
1. Clone the repository: `git clone https://github.com/Asmajavaid1270/Flyrank-ML-Internship`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the notebook/pipeline: Execute cells sequentially in `work/notebooks/capstone.ipynb`.

## 3. Usage Examples
* Running feature extraction on custom domain data partitions.
* Generating predictive volatility scores to flag underperforming URLs.

## 4. Architecture Sketch
`Raw SERP Logs` ➔ `Feature Engineering (Pandas/Scikit-Learn)` ➔ `Temporal Train/Val/Test Split` ➔ `Gradient Boosting Regression Model` ➔ `Actionable Optimization Playbook`

## 5. v2 Eval Results
* **Root Mean Squared Error (RMSE):** Improved from baseline 4.35 to 3.73 (14.2% error reduction).
* **Mean Absolute Error (MAE):** Improved from 3.12 to 2.64 (15.4% improvement).
* **Directional Accuracy:** Increased from 52.4% to 68.9%.

## 6. Limitations
* **Causality Constraints:** Due to unobserved external search engine algorithm updates, the model cannot claim direct causal relationships between isolated page edits and ranking changes.

## Transparency & AI Collaboration Note
Developed by Asma Javaid as part of the FlyRank ML Internship. AI tools were used as technical thinking partners for code structuring, while all data splits, evaluation metrics, and validations were independently verified.
