# 📉 Predictive Analytics for Employee Attrition Using ML and BI Tools

## 📝 Overview

**Predictive Analytics for Employee Attrition** is a full-stack analytics project that applies machine learning, business intelligence, and statistical techniques to forecast and understand why employees leave an organization. The goal is not only to predict attrition with accuracy but also to uncover actionable insights that can guide HR strategy and improve employee retention.

This project was developed as part of my MBA specialization in Business Analytics. It brings together structured HR data, real-world business context, and hands-on data science methods into one integrated solution that can serve as a playbook for any HR analytics team.

---

## 📂 Project Structure
```
Predictive-Analytics-for-Employee-Attrition/
│── 📂 DATA # Raw and cleaned datasets
│── 📂 Documentation # PDF/Docx exports of EDA, SQL, ML logic
│── 📂 EDA-Visualization # Graphs, heatmaps, boxplots from EDA.ipynb
│── 📂 ML_Modeling-Visualization # SHAP plots, confusion matrices, ROC curves
│── 📂 Power BI Dashboard # Screenshots and .pbix file for HR dashboards
│── 📂 SQL Queries Results # SQLite outputs and insights
│── 📄 DataProcessing.ipynb # Data cleaning, transformation, feature engineering
│── 📄 EDA.ipynb # Exploratory Data Analysis with visualizations
│── 📄 ML Modeling.ipynb # Logistic, Random Forest, SVM, XGBoost, ANN models
│── 📄 SQL Queries using sqlite3.ipynb # SQL-based segmentation and analysis
│── 📄 Statistical Analysis.xlsx # Hypothesis testing and descriptive stats
│── 📄 EmployeeAttrition_PredictiveDashboard.pbix # Live BI dashboard
│── 📄 attrition_analysis.db # SQLite database used in project
│── 📄 INSIGHTS & RECOMMENDATIONS.md # Strategic insights, HR solutions, executive takeaways
│── 📄 README.md # This file
```
---

## 💻 Technologies Used

- **Python** (pandas, seaborn, matplotlib, sklearn, xgboost, shap, imblearn)
- **SQL** (SQLite3 via Python)
- **Power BI** (interactive dashboards & slicers)
- **Excel** (statistical analysis, pivot tables, z-test, ANOVA)
- **Jupyter Notebook** (main development environment)

---

## 🗃️ Dataset Description

This project uses the popular IBM HR Employee Attrition dataset containing:

- **1470 employee records**  
- **50 variables**, including:
  - Demographics (Age, Gender, MaritalStatus)
  - Job & Compensation (JobRole, Department, MonthlyIncome, JobLevel)
  - Behavior (OverTime, BusinessTravel, YearsAtCompany, YearsSinceLastPromotion)
  - Feedback metrics (JobSatisfaction, WorkLifeBalance, PerformanceRating)

The dataset has been extensively cleaned, with **no column dropped**, and enhanced with additional features like:

- `AgeGroup`
- `TenureBucket`
- `PromotionStatus`
- `IncomeBand`

---

## 🛠️ Data Processing & Transformation

Handled in `DataProcessing.ipynb`:
- Nulls, dtypes, and outliers resolved
- Features binned and encoded (e.g., AgeGroup, TenureBucket)
- No features dropped—dimensionality retained for maximum insight
- SMOTE applied to balance attrition classes

---

## 📊 Exploratory Data Analysis (EDA)

Conducted in `EDA.ipynb` and visualized in `/EDA-Visualization`:
- Attrition rate: **16.2% overall**
- Key drivers uncovered through bar charts, boxplots, violin plots, and heatmaps:
  - Overtime → 30.5% attrition
  - Tenure <2 years → 25% attrition
  - Monthly income under ₹5000 → high exit risk
  - Sales & Lab Tech roles → highest churn

---

## 📈 Statistical Analysis

Covered in `Statistical Analysis.xlsx`:
- **T-tests, ANOVA, Chi-Square, Z-tests**
- Significant findings (p < 0.05):
  - Income, Distance from Home, WorkLifeBalance
  - Overtime & Business Travel show strong correlation with attrition
- Used Excel pivots to visualize attrition by age, job role, and satisfaction levels

---

## 🤖 Machine Learning Models

Implemented in `ML Modeling.ipynb`:
- Models tested:
  - Logistic Regression
  - Random Forest
  - Support Vector Machine
  - XGBoost (Best Performance)
  - Artificial Neural Network (ANN)
- **XGBoost** was the most balanced:
  - Accuracy: 86.4%
  - Precision: 65.2%
  - Recall: 31.9%
  - F1 Score: 42.8%
  - AUC: 0.86

Explainability was provided using **SHAP** values to interpret individual predictions.

---

## 🧠 SQL Analysis

Conducted in `SQL Queries using sqlite3.ipynb` and `/SQL Queries Results`:
- Segmented data by:
  - Tenure buckets
  - Promotion delays
  - Travel frequency
  - Risk clusters
- Highlighted vulnerable employee segments (e.g., young, high performer, underpaid)
- Showed leavers earned ₹2,045 less monthly than stayers

---

## 📊 Power BI Dashboard

Available as `.pbix` in `/Power BI Dashboard`, with images in the same folder:
- Filters by Job Role, Travel, Tenure, Marital Status
- KPI cards: Attrition %, Avg Income, Avg Tenure
- Visuals: Heatmaps, bar charts, pie charts, dynamic risk matrix
- Built for HR stakeholders to take **real-time, data-backed decisions**

---

## 🚀 Key Insights & Recommendations

Found in `INSIGHTS & RECOMMENDATIONS.md`:
- 10 key drivers of attrition ranked
- Department- and role-specific risks
- Actionable solutions for HR teams:
  - “Stay 2, Grow 2” early-career retention plan
  - Salary audits by job level
  - Remote flexibility for frequent travelers
  - Predictive dashboards with alert flags

---

## 🧩 How to Run This Project

1. **Clone the repo:**
```bash
git clone https://github.com/himanshudeol/Predictive-Analytics-for-Employee-Attrition-Using-ML-and-BI-Tools.git
cd Predictive-Analytics-for-Employee-Attrition-Using-ML-and-BI-Tools
```
2. **Install requirements:**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost shap imblearn jupyter
```
3. **Run notebooks in order:**

  - ```DataProcessing.ipynb```
  - ```EDA.ipynb```
  - ```ML Modeling.ipynb```
  - ```SQL Queries using sqlite3.ipynb```
4. **Open the BI Dashboard:**
  - Use ```EmployeeAttrition_PredictiveDashboard.pbix``` in Power BI Desktop.

---

## 🔭 Future Improvements
- Integrate timestamp data to track attrition trends over time
- Build a Streamlit app for real-time model deployment
- Use external HR benchmarks for smarter salary insights
- Add engagement surveys or sentiment analysis via NLP

---

## 📜 License
Open for academic and educational use. Attribution appreciated.

© 2025 Himanshu Deol – MBA Business Analytics

---

## 📬 Contributions & Feedback
I welcome discussions, suggestions, and collaborations.

If this project resonates with you or helps you, please ⭐ star the repo and feel free to open issues or pull requests.

Let's make HR smarter, not harder. 🚀
