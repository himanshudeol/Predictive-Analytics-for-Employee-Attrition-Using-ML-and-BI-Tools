## 📌 Purpose of This Guide

This guide walks you through how to set up, run, and explore the full scope of the project **“Predictive Analytics for Employee Attrition Using ML and BI Tools.”** Whether you're a data analyst, an HR strategist, or a fellow MBA student diving into workforce analytics, this manual ensures that you can reproduce the entire project environment on your local machine—from data cleaning and EDA to predictive modeling, SQL analysis, and Power BI dashboarding.

---

## 💻 What You’ll Need Before You Start

To make the most of this project, make sure you have the following tools installed:

### 🔧 Core Requirements

| Tool | Purpose |
|------|---------|
| Python 3.8+ | For running notebooks and ML models |
| Jupyter Notebook | Interactive notebook environment |
| Power BI Desktop | For visualizing the HR dashboard |
| Git | To clone the repository |

### 📦 Python Libraries

Install these libraries in your environment (using pip or conda):

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost shap imbalanced-learn sqlite3 openpyxl jupyter
````

---

## 📂 Folder Overview

You should see this structure after cloning:

```
📁 Predictive-Analytics-for-Employee-Attrition
│── DataProcessing.ipynb
│── EDA.ipynb
│── ML Modeling.ipynb
│── SQL Queries using sqlite3.ipynb
│── Statistical Analysis.xlsx
│── EmployeeAttrition_PredictiveDashboard.pbix
│── attrition_analysis.db
│── README.md
│── HOW_TO_RUN.md
│── INSIGHTS & RECOMMENDATIONS.md
│── 📂 DATA/
│── 📂 Documentation/
│── 📂 EDA-Visualization/
│── 📂 ML_Modeling-Visualization/
│── 📂 Power BI Dashboard/
│── 📂 SQL Queries Results/
```

---

## 🚀 Step-by-Step: Run the Project

### 🔹 Step 1: Clone the Repository

First, bring the project into your local environment:

```bash
git clone https://github.com/himanshudeol/Predictive-Analytics-for-Employee-Attrition-Using-ML-and-BI-Tools.git
cd Predictive-Analytics-for-Employee-Attrition-Using-ML-and-BI-Tools
```

---

### 🔹 Step 2: Open Jupyter Lab or Notebook

Start Jupyter in your preferred working directory:

```bash
jupyter notebook
```

You’ll see the project files listed in your browser.

---

### 🔹 Step 3: Run the Notebooks in Sequence

Here’s the order and what each notebook does:

#### ✅ 1. `DataProcessing.ipynb`

* Cleans the raw dataset
* Handles nulls and outliers
* Encodes categorical variables
* Bins features like AgeGroup and TenureBucket
* Applies SMOTE for class balance

🗃️ Output: A cleaned dataframe used for ML, SQL, and BI components

---

#### ✅ 2. `EDA.ipynb`

* Explores attrition trends with graphs
* Compares attrition by age, gender, role, income, overtime, etc.
* Visualizes distributions, boxplots, and heatmaps

📊 Output: Plots saved to `/EDA-Visualization`

---

#### ✅ 3. `ML Modeling.ipynb`

* Runs 5 ML models (Logistic Regression, Random Forest, SVM, XGBoost, ANN)
* Evaluates performance using accuracy, recall, F1 score, AUC
* Uses SHAP for explainability

🏆 Output:

* Best model (XGBoost)
* Feature importance
* Model evaluation graphs in `/ML_Modeling-Visualization`

---

#### ✅ 4. `SQL Queries using sqlite3.ipynb`

* Queries HR attrition database using SQLite3
* Segments risk by tenure, travel, promotion history
* Identifies high-risk profiles for HR follow-up

🛢️ Input: `attrition_analysis.db`
📄 Output: Tables and graphs in `/SQL Queries Results`

---

### 🔹 Step 4: Open the Excel File (Statistical Analysis)

#### 🧪 `Statistical Analysis.xlsx`

* T-Tests, Z-Tests, ANOVA, Chi-Square
* Pivot tables by department, tenure, and age
* Summary charts for quick insights

📌 This file supports your statistical narrative and adds credibility to findings.

---

### 🔹 Step 5: Explore the Power BI Dashboard

#### 📈 `EmployeeAttrition_PredictiveDashboard.pbix`

Steps:

1. Open Power BI Desktop
2. Load the `.pbix` file
3. Use slicers to filter attrition by:

   * Job Role
   * Travel Frequency
   * Overtime
   * Marital Status
   * TenureBucket
4. Observe how KPIs (attrition %, income, satisfaction) shift

🧠 **This dashboard is built for real-time HR decision-making.**

---

## 💡 Pro Tips

* 🔁 **Refresh Power BI dashboard** after modifying SQL data or predictions
* 📊 **Use SHAP plots** to justify ML decisions to non-technical stakeholders
* 📚 **Refer to `INSIGHTS & RECOMMENDATIONS.md`** for strategic solutions
* 🔄 **Retrain ML model monthly** if using this in real-world HRMS workflows

---

## 🔒 Optional: Connecting to Your Own Dataset

If you want to plug in your own HR data:

1. Match the schema of the original dataset (column names, structure)
2. Replace files in the `/DATA` folder
3. Re-run `DataProcessing.ipynb` and follow the same sequence

💼 Now your organization can benefit from predictive HR!

---

## 📩 Questions, Suggestions, or Feedback?

Feel free to reach out via GitHub Issues or connect on LinkedIn.
This project is designed to be educational, replicable, and customizable.

---

👨‍💻 *Created by:* **Himanshu Deol**

🎓 *MBA (Business Analytics)*

https://www.linkedin.com/in/himanshudeol/
