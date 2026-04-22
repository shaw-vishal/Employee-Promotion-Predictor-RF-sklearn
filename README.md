# 🧠 Employee Promotion Prediction (HR Analytics)

## 📍 Overview

Promotion decisions are critical for employee motivation, retention, and organizational growth. However, manual evaluation across multiple parameters often leads to delays and inconsistencies.

This project builds a machine learning classification system to assist HR teams in identifying employees with a high likelihood of promotion using historical workforce data.

---

## 🎯 Business Objective

- Reduce time taken in promotion decisions
- Improve fairness and consistency in evaluations
- Identify high-potential employees early
- Support HR with data-driven recommendations

---

## 📊 Problem Type

**Supervised Learning → Binary Classification**

**Target Variable:**
- `is_promoted` → (0 = No, 1 = Yes)

---

## 🗂 Dataset Description

| Feature | Description |
|---|---|
| `employee_id` | Unique employee identifier |
| `department` | Department of employee |
| `region` | Work location |
| `education` | Education level |
| `gender` | Gender |
| `recruitment_channel` | Hiring source |
| `no_of_trainings` | Trainings completed last year |
| `age` | Employee age |
| `previous_year_rating` | Performance rating |
| `length_of_service` | Tenure (years) |
| `awards_won` | Awards indicator |
| `avg_training_score` | Training performance |
| `is_promoted` | **Target** |

---

## 🔎 Key Challenges

- **Class Imbalance** → Very few employees are promoted
- **Missing Values** → Especially in ratings and education
- **Categorical Variables** → Multiple encoded features
- **Business Interpretation** → Not just accuracy, but actionable insights

---

## ⚙️ Approach

### 1. Data Preprocessing
- Missing value imputation (Median + Mode)
- Label Encoding for categorical features
- Feature scaling using StandardScaler

### 2. Exploratory Analysis
- Promotion distribution (high imbalance observed)
- Correlation analysis
- Feature influence trends

### 3. Model Building
- **Random Forest Classifier**
  - Handles non-linear relationships
  - Robust to noise and feature interactions
  - Provides feature importance

---

## 📈 Model Evaluation

**Metrics Used:**
- Accuracy
- Precision / Recall / F1-score
- Confusion Matrix

> ⚠️ **Note:** In HR use-cases, **Recall (True Positives)** is often more important than accuracy — missing a promotable employee is a costly mistake.

---

## 🔑 Key Insights

- 📊 **Training Score** is the strongest predictor
- 🏆 Employees with awards have significantly higher promotion chances
- ⭐ Previous year ratings strongly correlate with promotion
- ⏳ Long tenure without performance growth reduces promotion likelihood
- 📉 Promotions are highly imbalanced, indicating strict selection

---

## 💡 Business Recommendations

- Invest in training programs to improve promotion readiness
- Build early identification systems for high performers
- Track employee stagnation in long-tenure roles
- Use model predictions as a decision-support tool, not a replacement

---

## 🛠 Tech Stack

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn

---

## 📁 Project Structure

```
├── employee_promotion.csv
├── employee_promotion_notebook.ipynb
├── README.md
```

---

## 🚀 Future Improvements

- Handle imbalance using **SMOTE** / Class Weights
- Try **XGBoost / LightGBM** for better performance
- Hyperparameter tuning (GridSearchCV / Optuna)
- Add **ROC-AUC curve** and threshold analysis
- Deploy as a simple **HR dashboard** (Streamlit)

---

## 👤 Author

**Vishal Shaw**  
Data Science | Business Strategy | GTM Thinking

- GitHub: [shaw-vishal](https://github.com/shaw-vishal)
- LinkedIn: [vishalshaw6](https://www.linkedin.com/in/vishalshaw6/)

---

> ⚠️ **Disclaimer:** This model is designed to assist HR decision-making, not replace human judgment.
