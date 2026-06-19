🏥 NovaGen Lab — Health Classification with ML

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/Domain-Healthcare%20AI-red?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge"/>
</p>

> **A predictive ML model that classifies individuals as healthy or unhealthy** based on diagnostic lab data — bringing AI to preventive healthcare.

---

## 📌 Project Overview

Early detection of health conditions dramatically improves patient outcomes and reduces treatment costs. **NovaGen Lab** applies machine learning to diagnostic data to classify individuals into health categories — enabling faster, data-driven clinical decision support.

This project simulates a real-world medical AI use case: training a classifier on lab test results to flag at-risk individuals before symptoms become critical.

---

## 🎯 Problem Statement

Given a patient's diagnostic lab results, predict:
- 🟢 **Healthy** — biomarkers are within normal range, no immediate risk
- 🔴 **Unhealthy** — biomarkers indicate an underlying condition or elevated risk

This is a **binary classification** problem with high real-world impact — an incorrect prediction can have serious consequences, making model precision and recall equally important.

---

## 🔍 Dataset Features

| Feature | Description |
|---|---|
| `Age` | Patient age |
| `Gender` | Male / Female |
| `BMI` | Body Mass Index |
| `Blood Glucose` | Fasting blood glucose level (mg/dL) |
| `Blood Pressure` | Systolic blood pressure (mmHg) |
| `Cholesterol` | Total cholesterol level (mg/dL) |
| `Hemoglobin` | Hemoglobin count (g/dL) |
| `WBC Count` | White blood cell count |
| `Insulin Level` | Fasting insulin level |
| `Heart Rate` | Resting heart rate (bpm) |
| `Health_Status` | **Target** — Healthy / Unhealthy |

---

## 🛠️ Tech Stack

- **Python 3.x**
- **Pandas** — data loading, cleaning, and manipulation
- **NumPy** — numerical operations
- **Matplotlib & Seaborn** — visualizations (distributions, boxplots, correlation heatmaps)
- **Scikit-learn** — classification models, preprocessing, cross-validation, evaluation metrics
- **Jupyter Notebook** — interactive analysis environment

---

## 🔄 ML Pipeline

```
Data Collection → EDA → Preprocessing → Model Training → Evaluation → Clinical Insight
```

1. **Exploratory Data Analysis** — understand distributions of each biomarker across healthy vs. unhealthy groups
2. **Data Cleaning** — handle missing values, detect and treat outliers using IQR method
3. **Feature Engineering** — normalize continuous variables, encode categorical ones
4. **Train-Test Split** — stratified 80/20 split to preserve class balance
5. **Model Training** — Logistic Regression, Decision Tree, and comparison
6. **Evaluation** — Accuracy, Precision, Recall, F1-Score, Confusion Matrix
7. **Feature Importance** — identify which lab values matter most

---

## 📊 Key EDA Findings

- **Blood Glucose** and **BMI** show the strongest separation between healthy and unhealthy groups
- **Cholesterol levels** above 240 mg/dL are strongly associated with unhealthy classification
- **Age** is a significant risk factor — unhealthy classification rate rises sharply after age 45
- **Hemoglobin** levels are notably lower in the unhealthy group, suggesting anaemia as a co-factor
- Correlation heatmap reveals moderate positive correlation between BMI and Blood Glucose

---

## 📈 Model Performance

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| Logistic Regression | ~85% | ~84% | ~86% | ~85% |
| Decision Tree | ~81% | ~80% | ~82% | ~81% |

> **Recall is critical here** — we prefer to minimize false negatives (missing an unhealthy patient) even at the cost of some false positives.

---

## 🧬 Why This Matters

In healthcare AI, interpretability is as important as accuracy. A model must not just predict correctly — it must show clinicians *which features* drove the prediction. This project uses:
- **Feature importance scores** to rank biomarker contribution
- **Confusion matrices** to understand error types (false positives vs. false negatives)
- **Threshold tuning** to favour recall over precision in clinical settings

---

## 🚀 How to Run

**1. Clone the repository**
```bash
git clone https://github.com/ayush10mishra-hash/novagen-lab-project.git
cd novagen-lab-project
```

**2. Install dependencies**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

**3. Launch the notebook**
```bash
jupyter notebook novagen.ipynb
```

**4. Run all cells** — the notebook guides you through the full pipeline from raw data to model evaluation.

---

## 📁 Project Structure

```
novagen-lab-project/
│
├── novagen.ipynb          # Main Jupyter notebook (EDA + Classification)
└── README.md              # Project documentation
```

---

## ⚠️ Disclaimer

This project is for **educational and research purposes only**. It is not intended for actual clinical use or as a substitute for professional medical advice, diagnosis, or treatment. Always consult a qualified healthcare provider for medical decisions.

---

## 🔮 Future Improvements

- [ ] Expand to multi-class classification (e.g. diabetes, hypertension, anaemia)
- [ ] Integrate Random Forest and XGBoost for better performance
- [ ] Add SHAP (SHapley Additive exPlanations) for model interpretability
- [ ] Build a Streamlit web app for clinician-friendly predictions
- [ ] Train on larger, publicly available medical datasets (e.g. UCI Heart Disease, PIMA Diabetes)

---

## 👤 Author

**Ayush Mishra** — AI & ML Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ayush-mishra-5b015635b)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/ayush10mishra-hash)

---

⭐ If you found this project useful, please consider giving it a star!

