# Analyzing Fatal Injury Patterns in Construction Incidents: An Explanatory Data Science Approach

## 🧭 Overview

This project investigates workplace injuries in the construction industry, with a focus on understanding the **factors associated with fatal outcomes**. Rather than predicting individual cases, the goal is to analyze patterns, explore relationships, and explain what types of injuries or conditions are more likely to result in death.

Key steps included:
- Exploratory Data Analysis: Injury pattern analysis by body part, nature of injury, and environmental/human/task-related factors
- Statsistical Testing: A/B testing using Fisher’s Exact Test to compare fatality rates during holidays vs. non-holidays
- Logistic regression to quantify how different features affect the likelihood of fatality
- Data Visualization using matplotlib and Power BI to bring insights to life

<p align="center">
  <img src="construction-image.jpg" alt="Incident Analysis Chart" width="600" height="400">
</p>


---

## 📦 Dataset

- **Source**: OSHA accident reports  
- **Size**: ~4,800 incidents  
- **Columns**: 25+ fields including injury type, body part affected, human/environmental factors, date, task assignment, etc.

- **Target Variable**: `Degree of Injury`  
  - Encoded as binary:  
    - `1` = Fatal  
    - `0` = Non-Fatal

- **Key Features Used**:
  - Nature of Injury  
  - Part of Body  
  - Event Type  
  - Human Factor  
  - Environmental Factor  
  - Task Assigned  
  - Is_Holiday  
  - Season

---

## 🔍 Exploratory Analysis Highlights

- 61% of incidents in the dataset resulted in fatalities.
- **Head, internal, and whole-body injuries** were much more likely to be fatal.
- **Fingers, hands, and limbs** were rarely fatal.
- Incidents on **holidays** showed slightly higher fatality odds but not statistically significant.
- Injury patterns showed meaningful **seasonal** and **task-based** trends.

---

## 🧪 Statistical Testing

To evaluate whether holidays are associated with higher fatality rates, a **Fisher’s Exact Test** was conducted.

- **Result**:  
  - Odds Ratio: 1.35  
  - P-value: 0.18  

> 🔹 Interpretation: There was no statistically significant evidence that fatal injuries are more likely to occur on holidays.

---

## 🤖 Explanatory Modeling: Logistic Regression

A logistic regression model was used to understand which features were **most strongly associated with fatal injuries**.

### ✅ Performance:
- **ROC AUC = 0.96** → Excellent ability to distinguish between fatal and non-fatal injuries

### 🔥 Top Features Associated with Fatalities:
| Feature                                      | Coefficient | Odds Ratio |
|----------------------------------------------|-------------|------------|
| Nature of Injury: Asphyxiation, Drowning     | +2.46       | ~11.7x     |
| Part of Body: Head                           | +2.14       | ~8.5x      |
| Part of Body: Whole Body                     | +2.02       | ~7.5x      |
| Part of Body: Internal Injuries              | +1.92       | ~6.8x      |
| Part of Body: Neck                           | +1.74       | ~5.7x      |

---

## 📊 Data Visualization

To complement the Python-based analysis, a Power BI dashboard was created to explore the data interactively and visually communicate the insights.

<p align="center">
  <img src="incidents-analysis.jpg" alt="Power BI Incident Analysis Dashboard" width="1000" height="400">
</p>

The dashboard includes:
- Total, fatal, and non-fatal incidents
- Most common injury types and affected body parts
- Environmental and human factors contributing to injuries
- Trends over time and filterable slicers for interactivity

--

## 💡 Key Takeaways

- Certain injury types and affected body parts carry significantly higher fatality risk.
- Logistic regression was effective as an **explanatory model**, not for forecasting but for interpretation.
- Statistical evidence did **not** support a significant difference in fatality rates on holidays.
- The project demonstrates the value of **explanatory data science** in high-risk industries like construction.

---

## 📊 Tools Used

- Python (pandas, scikit-learn, matplotlib, seaborn, statsmodels)
- Jupyter Notebook
- Power BI (for dashboard visualizations)
- Git & GitHub

---

## Contact

- Nafisat Ibrahim

