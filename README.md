# Patient Readmission Risk Prediction

## 📓 Notebooks

You can view the work in three ways:

- **GitHub Preview**
  - [Modeling](notebooks/02_modeling.ipynb)

- **Nbviewer (better rendering)**
  - [Modeling via Nbviewer](https://nbviewer.org/url/raw.githubusercontent.com/tiefads/patient-readmission-risk/main/notebooks/02_modeling.ipynb)

- **Static HTML (always works)**
  - [Modeling (HTML export)](reports/02_modeling.html)


Predicting 30-day hospital readmissions using the **Diabetes 130-US Hospitals** dataset (UCI Machine Learning Repository).

---

## 🚑 Why it matters
Hospital readmissions within 30 days are costly and stressful for patients.  
By predicting readmission risk, hospitals can prioritize follow-ups and allocate resources where they’re needed most.

---

## 📊 Dataset
- **Source:** [UCI ML Repository — Diabetes 130-US Hospitals](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008)  
- ~101,766 encounters, 50+ features  
- Features: demographics, diagnoses (ICD-9), lab results, medications, encounter info  
- Target: **readmitted within 30 days (yes/no)**

---

## 🛠️ Approach
1. **EDA:** explored demographics, missingness, and categorical distributions.  
2. **Baseline model:** Logistic Regression  
   - AUROC: 0.646  
   - AUPRC: 0.205  
3. **Improved model:** XGBoost (tree-based boosting)  
   - AUROC: 0.682  
   - AUPRC: 0.232  
4. **Thresholding:** Flagging top 10% high-risk patients:  
   - Precision ≈ 0.27 vs baseline prevalence 0.11  
   - Recall ≈ 0.24  
5. **Explainability:** SHAP values identified key drivers (time in hospital, number of medications, diabetes med usage).  
6. **Deployment readiness:** Saved full preprocessing + model pipeline with `joblib`.

---

## 📂 Project structure
# Patient Readmission Risk Prediction
