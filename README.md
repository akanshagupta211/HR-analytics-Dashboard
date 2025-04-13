# HR Analytics Dashboard using Power BI and Power Query

This project presents an interactive HR Analytics Dashboard built using Power BI, Power Query, and DAX. It offers actionable insights into employee attrition trends, job satisfaction, and workforce demographics, enabling data-driven HR decision-making.

---

## 🔧 Tools & Technologies Used
- Power BI
- Power Query (for data preprocessing)
- DAX (Data Analysis Expressions)
- Data Modeling

---

## 📂 Dataset Overview
The dataset contains employee-level information including:
- Age, Gender, Department, Education, Salary
- Job Role, Job Satisfaction, Years at Company
- Attrition Status (Yes/No)

Data preprocessing was done using Power Query to:
- Handle missing values using mean imputation or row removal
- Standardize categorical values (e.g., Job Role)
- Remove duplicates and correct data types
- Engineer features like Age Group and Salary Slabs

---

## 📊 Key Dashboard Features & Visualizations

- **KPI Cards:** Average Age, Average Salary, Average Years at Company, Attrition Rate, Total Employees
- **Filters:** Department-based filters – Sales, HR, R&D

### Visualizations Used:
1. **Donut Chart** – Attrition by Education Level  
2. **Stacked Column Chart** – Attrition by Age & Gender  
3. **Matrix Chart** – Job Role vs. Job Satisfaction (Avg. rating: 2.5/4)  
4. **Stacked Bar Chart** – Attrition by Salary Slab  
5. **Area Chart** – Attrition by Tenure (50% leave within 5 years)  
6. **Stacked Bar Chart** – Attrition by Job Role  

---

## ⚙️ DAX Measures & Functions Used
- `Attrition Rate = DIVIDE(COUNT(Employee[Attrition = "Yes"]), COUNT(Employee[EmpID]))`
- `Running Total = CALCULATE(COUNT(Employee[EmpID]), FILTER(ALL(Employee[Year]), Employee[Year] <= MAX(Employee[Year])))`
- `Avg Income = AVERAGE(Employee[MonthlyIncome])`
- `Work-Life Balance = AVERAGE(Employee[WorkLifeBalance])`

---

## 📈 Key Insights
- **77% higher attrition among males** (1.77 males leave for every female)
- **Employees aged 25-35 and earning below $5,000** show highest attrition (60%)
- **Customer-facing roles** have lower satisfaction, with an average rating of 2.5/4
- **50% of employees leave within their first 5 years**, highlighting the need for retention strategies

---

## 📁 Dashboard Access
📌 *Download the PBIX file and open in Power BI Desktop for interactive use.*
