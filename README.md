# 📉 Customer Churn Prediction — Telecom Industry

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.2%2B-orange?logo=scikit-learn)
![SHAP](https://img.shields.io/badge/SHAP-Explainability-red)
![License](https://img.shields.io/badge/License-MIT-green)

> **End-to-end churn analysis pipeline** — from EDA and hypothesis testing to a tuned Random Forest model with SHAP explainability, delivering actionable retention strategies projected to reduce churn by ~15%.

---

## 🎯 Project Overview

This project analyzes customer churn in a telecom company across **5,000+ customer records**, uncovering the key behavioral and demographic signals that drive churn. The final model achieves **87% accuracy** and **0.91 AUC-ROC**, with SHAP used to convert the black-box model into interpretable business intelligence.

---

## 📊 Key Results

| Metric | Score |
|--------|-------|
| Accuracy | **87%** |
| AUC-ROC | **0.91** |
| Top churn driver | Complaint Frequency |
| Projected churn reduction | ~15% |

---

## 🔍 Dataset

| Feature | Type | Description |
|---------|------|-------------|
| Age | Numerical | Customer age (18–80) |
| Gender | Categorical | Male / Female |
| Tenure | Numerical | Months as a customer |
| ServiceType | Categorical | Prepaid / Postpaid / Fiber |
| Complaints | Numerical | Number of complaints raised |
| MonthlySpend | Numerical | Average monthly bill (INR) |
| RecentlyOptedOffers | Binary | 1 = opted in to a recent offer |
| Churn | Binary | **Target** — 1 = churned |

---

## 🧪 Hypotheses Tested

| Hypothesis | Result |
|------------|--------|
| H1: High complaint frequency increases churn probability | ✅ Confirmed (Chi-Square, p < 0.001) |
| H2: High spend + tenure < 12 months → higher churn | ✅ Confirmed (2.3x relative risk) |
| H3: Targeted offers reduce churn only for tenure > 2 years | ✅ Confirmed |

---

## 🛠️ Tech Stack

- **Language:** Python 3.9+
- **ML:** Scikit-learn — Random Forest, GridSearchCV, 5-fold CV
- **Explainability:** SHAP (TreeExplainer — beeswarm + bar plots)
- **EDA:** Pandas, Matplotlib, Seaborn
- **Stats:** SciPy (chi-square significance testing)

---

## 📁 Project Structure

```
customer-churn-prediction/
├── Customer_Churn_Analysis_KaranSH.ipynb   # Main notebook (end-to-end pipeline)
├── requirements.txt                         # Python dependencies
├── report/
│   └── Analysis_of_Customer_Churn.pdf      # Project report
└── README.md
```

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/karansiva14/customer-churn-prediction.git
cd customer-churn-prediction

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the notebook
jupyter notebook Customer_Churn_Analysis_KaranSH.ipynb
```

---

## 📈 Notebook Sections

1. **Imports & Setup** — libraries, random seed, plot config
2. **Dataset Generation** — 5,000 synthetic telecom records with realistic churn signals
3. **EDA** — distribution plots, churn by service/age/gender, correlation heatmap
4. **Feature Engineering** — ComplaintRate, HighSpendLowTenure flag, SeniorFlag, LifetimeValue
5. **Hypothesis Testing** — chi-square test + group-level churn rate comparisons
6. **Model Training** — Random Forest + GridSearchCV (5-fold CV, AUC-ROC scoring)
7. **Evaluation** — confusion matrix, ROC curve, cross-validation stability
8. **SHAP Explainability** — beeswarm plot, bar importance, top driver ranking
9. **Business Recommendations** — 4 targeted retention strategies

---

## 💡 Top Churn Drivers (SHAP)

1. **Complaint Frequency** — customers with 3+ complaints churn at extremely high rates
2. **Tenure < 6 months** — new customers are the most vulnerable segment
3. **High Spend + Low Tenure** — risky combination of high value + low loyalty
4. **Monthly Spend** — senior customers with high bills churn disproportionately

---

## 📌 Business Recommendations

| Strategy | Target Segment | Expected Impact |
|----------|---------------|-----------------|
| Proactive outreach within 48hrs | Customers with 2+ complaints | Reduce complaint-driven churn |
| Onboarding loyalty package | New customers (Month 1–3) | Reduce early dropout |
| Retention offer trigger | High-spend customers, tenure < 12m | Protect high-value new customers |
| Senior support plan | Age 60+, high monthly spend | Reduce senior churn |

> Implementing all four strategies is projected to reduce overall churn by **~15%**.

---

## 👤 Author

**Karan S H**  
AI/ML Engineer | IIT Minor in AI & Data Science  
📧 karansmiley14@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/karan1414) · [GitHub](https://github.com/karansiva14)

---

## 📄 License

This project is licensed under the MIT License.
