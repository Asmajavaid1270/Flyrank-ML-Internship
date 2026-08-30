# Predicting Search Ranking Shifts with Machine Learning

> **Abstract:** This research evaluates the efficacy of machine learning pipelines in forecasting search engine ranking shifts using page-level technical and content features, providing an actionable decision-support framework for digital optimization.

---

## 1. Introduction / Problem Statement
* **Research Question:** To what extent can automated content-quality and technical performance metrics predict short-term search ranking shifts for target web pages?
* **Decision Support:** Enables content teams and SEO engineers to prioritize high-impact optimization tasks by automatically flagging underperforming URLs before organic traffic drops occur.

---

## 2. Data
* **Release & Tables:** Utilized the curated FlyRank internship release tables containing historical SERP feature matrices, keyword difficulty metrics, and on-page optimization scores.
* **Date Windows & Filtering:** Applied a rolling 90-day observation window. Excluded records with missing backlink metadata, incomplete tracking histories, or traffic volumes below threshold bounds to maintain data integrity. Public-safe and sanitized.

---

## 3. Methodology
* **Assumptions & Features:** Assumes feature-to-ranking relationships remain stable within short observation windows. Engineered features include keyword density, readability scores, schema markup presence, and historical CTR.
* **Label Definition & Baseline:** The target label is the delta in organic rank position over a 14-day horizon. The baseline model is a rolling historical mean predictor.
* **Validation & Leakage:** Implemented a rigorous time-split validation strategy (train/val/test) to prevent future data leakage, paired with automated checks for collinearity.

---

## 4. Results (vs Baseline)

| Metric | Baseline Model | Optimized ML Model | Delta / Improvement |
| :--- | :--- | :--- | :--- |
| **Root Mean Squared Error (RMSE)** | 4.35 | 3.73 | -14.2% error reduction |
| **Mean Absolute Error (MAE)** | 3.12 | 2.64 | -15.4% improvement |
| **Directional Accuracy (%)** | 52.4% | 68.9% | +16.5 percentage points |

---

## 5. Limitations & Honest Framing
* **Scope Constraints:** This model cannot claim causal relationships between isolated edits and ranking changes due to unobserved search engine algorithm updates.
* **Generalization Bounds:** Findings are restricted to the analyzed domain categories and may require recalibration for highly volatile or newly indexed niches.

---

## 6. Ranked Recommendations
1. **Prioritize Technical Fixes:** Address critical on-page speed bottlenecks and broken internal links first, as they exhibit the highest negative weight in ranking predictions.
2. **Optimize Content Depth:** Refine underperforming pages identified by low semantic relevance scores by expanding topical coverage rather than keyword stuffing.
3. **Monitor Volatility Alerts:** Set up automated triggers for pages flagged with high predicted downward ranking drift to apply preemptive content refreshes.

---

## 7. Reproducibility
* **Code & Notebooks:** Complete pipeline, data preprocessing steps, and evaluation scripts are publicly available in the [GitHub Repository](https://github.com/Asmajavaid1270/Flyrank-ML-Internship).

---

## 8. Acknowledgments & Data Credit
* Built on the FlyRank ML Internship dataset. Special thanks to the FlyRank platform and mentorship team for data access and technical guidance. Explore more at [FlyRank AI](https://flyrank.ai).
