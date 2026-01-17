# 📘 Study-Smarter  
### Data-Driven Insights into Student Performance

An Advanced Data Analytics course project that combines **predictive modeling** and **causal inference** to understand and improve student academic performance.

---

## 📌 Project Overview

Student performance is influenced by multiple academic, demographic, and social factors.  
This project adopts a **dual-pronged analytical approach**:

1. **Prediction** – Estimate a student’s final grade (G3) using machine learning models.
2. **Causal Inference** – Determine whether *higher study time actually causes better academic outcomes*, rather than merely being correlated.

---

## 🎯 Problem Statement

To analyze student academic performance by:

- Predicting final grades (G3) using regression models  
- Estimating the **causal impact of high study time (≥ 2 hours)** on academic performance  
- Controlling for confounding variables such as failures, absences, and prior grades

---

## ✨ Why This Project Is Unique

- 🔁 **Dual Analysis Framework**
  - Predictive Modeling → *What will happen?*
  - Causal Inference → *Why does it happen?*

- 🧠 **Beyond Correlation**
  - Uses **Propensity Score Matching (PSM)** and  
    **Inverse Probability Weighting (IPW)**

- 📊 **Heterogeneity Analysis**
  - Studies how effects differ by:
    - Gender
    - Number of past academic failures

- 🧩 **Merged Dataset**
  - Mathematics + Portuguese datasets combined
  - Total **1,044 students**

---

## 📂 Dataset Information

**Source:**  
UCI Machine Learning Repository – Student Performance Dataset  
(P. Cortez & A. Silva)

**Size:**
- 1,044 students
- 33 original attributes

**Feature Categories:**

- **Academic**
  - G1, G2, G3
  - studytime
  - failures
  - absences

- **Demographic**
  - age, sex, address
  - mother/father job

- **Lifestyle & Social**
  - freetime, goout
  - Dalc (weekday alcohol)
  - Walc (weekend alcohol)
  - health

---

## 🧠 Methodology

### 1️⃣ Data Preprocessing
- Dataset merging
- Missing value handling
- Encoding categorical variables
- Feature scaling

---

### 2️⃣ Predictive Modeling

**Models Used:**
- Random Forest Regressor
- Lasso Regression

**Target Variable:**
- Final Grade (G3)

**Evaluation Metrics:**
- R² Score
- RMSE
- Cross-validation performance

---

### 3️⃣ Causal Inference

**Treatment Variable:**
- High Study Time (≥ 2 hours)

**Methods Applied:**
- Propensity Score Matching (PSM)
- Inverse Probability Weighting (IPW)

**Confounders Controlled:**
- Past failures
- Absences
- Previous grades
- Demographic factors

---

## 📈 Results

### 🔍 Predictive Modeling

| Metric | Value |
|------|------|
| Best Model | Random Forest Regressor |
| Test R² | 0.178 |
| RMSE | 3.491 |
| Cross-Validation R² | 0.123 |

> ⚠️ Predicting exact grades is difficult due to high human variability.

---

### 🔬 Causal Inference Findings

- **Average Treatment Effect (ATE):**
  - High study time increases final grade by **~0.56 points**

- **Statistical Significance:**
  - IPW: *p = 0.017*

✅ Confirms that **studying more actually causes improvement**, not just correlation.

---

## 📊 Key Visualizations

- SHAP Feature Importance
  - `absences` and `failures` → strongest negative factors
  - `high_study` → positive contributor

- Propensity Score Overlap
  - Confirms valid matching between treated and control groups

---


## 📁 Repository Structure

```text
Study-Smarter/
├── ADA_MINI/
│   └── models/
│       ├── best_model.pkl          # Serialized trained model
│       └── best_model_reduced.pkl  # Optimized/reduced version of the model
├── ada-project-final.ipynb         # Main Jupyter Notebook with analysis & modeling
├── ResearchInformation3.csv        # Primary research dataset
├── student-mat (1).csv             # Student performance data (Math)
├── student-por (1).csv             # Student performance data (Portuguese)
├── ADA_CourseProject (1).pptx      # Project presentation slides
├── IEEE_Project_Report.docx        # Formal technical report (IEEE Format)
└── README.md                       # Project documentation
```
---

## 👥 Team Members

- **Abhishek P** – PES2UG23AM002  
- **Adyaa G B** – PES2UG23AM006  
- **Adyanth S** – PES2UG23AM007  
- **Harsha** – PES2UG23AM042  

Department of Computer Science and Engineering (AI & ML)  
PES University

---

## 📚 Key Learnings

- Predictive models alone are insufficient for decision-making
- Causal inference provides actionable insights
- Human academic performance contains high uncertainty
- Interpretability (SHAP) is crucial for trust in ML models

---

## ⚠️ Limitations & Future Work

**Limitations**
- Self-reported study time
- Lack of psychological and behavioral attributes

**Future Enhancements**
- Advanced causal estimators (Double ML, Causal Forests)
- Personalized intervention recommendations
- Integration with academic advisory systems

---

## 📖 References

1. P. Cortez & A. Silva – UCI Student Performance Dataset  
2. Judea Pearl – *Causality*  
3. Lundberg & Lee – SHAP Interpretability  
4. Kuh – Student Success in Higher Education  

---

## 🏁 Conclusion

While predicting exact academic grades remains challenging,  
this project demonstrates that **causal inference provides meaningful and actionable educational insights**.

High study time is not just correlated — it **causally improves student performance**.

