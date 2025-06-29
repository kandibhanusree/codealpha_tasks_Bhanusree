# codealpha_tasks_Bhanusree

# 🧠 HR Analytics Dashboard using Power BI

This repository contains a Power BI dashboard project analyzing employee attrition using the [WA_Fn-UseC_-HR-Employee-Attrition](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) dataset.

---

## 📊 Dashboard Overview

The Power BI report answers key HR questions like:
- What is the attrition rate?
- What are the common factors influencing attrition?
- How do different departments, job roles, and education levels correlate with attrition?

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `HR_Attrition_Analysis.pbix` | Power BI Dashboard |
| `README.md` | Project documentation |
| `images/` | Screenshots of the dashboard (optional) |

---

## 📌 Features

- Interactive slicers: Gender, Department, Education Field, etc.
- Visuals: Bar charts, Pie charts, KPI cards, Donut charts
- DAX Measures for KPIs and filters
- Drillthrough page for employee-level details

---

## 🔍 DAX Queries Used

```dax
-- Total Employees
Total Employees = COUNTROWS('HR_Data')

-- Total Attrition
Total Attrition = CALCULATE(COUNTROWS('HR_Data'), 'HR_Data'[Attrition] = "Yes")

-- Attrition Rate (%)
Attrition Rate (%) = 
DIVIDE([Total Attrition], [Total Employees], 0)

-- Active Employees
Active Employees = CALCULATE(COUNTROWS('HR_Data'), 'HR_Data'[Attrition] = "No")

-- Average Age of Employees
Average Age = AVERAGE('HR_Data'[Age])

-- Average Daily Rate
Average Daily Rate = AVERAGE('HR_Data'[DailyRate])

-- Gender Count (Male)
Male Count = CALCULATE(COUNTROWS('HR_Data'), 'HR_Data'[Gender] = "Male")

-- Gender Count (Female)
Female Count = CALCULATE(COUNTROWS('HR_Data'), 'HR_Data'[Gender] = "Female")



How to Use
Download the .pbix file

Open using Power BI Desktop

Load the data or replace it with your HR dataset

Explore, interact with visuals, or edit for your needs

🛠 Tools & Technologies
Power BI Desktop

DAX (Data Analysis Expressions)

Kaggle HR Analytics Dataset

GitHub

-> Dashboard Preview

You can upload screenshots in an images/ folder and link them here.

-> Contact
If you have questions or suggestions:

📧 Email: kandibhanusree@gmail.com

💼 LinkedIn: (https://www.linkedin.com/in/kandi-bhanusree-b15b29160/)
