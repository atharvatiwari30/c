## 📊 Employee Yearly Analysis - Power BI Dashboard
🔍 Overview
This Power BI dashboard provides an in-depth analysis of employee data over the course of a year. It helps HR teams, business analysts, and management track employee trends including hiring, attrition, department performance, and workforce distribution.

## ✅ Features
🚹 Gender-wise employee distribution

🏢 Department-wise headcount and salary insights

🗓️ Monthly Hiring vs Attrition trends

📍 Location-wise employee mapping

💸 Average salary & salary distribution

⭐ Performance rating insights

📈 Year-over-Year comparison of key metrics

📌 Slicers for Department, Year, Gender, and Location

## 🧾 Dataset Structure
Column Name	Description
EmployeeID	Unique identifier for each employee
Name	Employee full name
Department	Department name (e.g., HR, Sales)
Designation	Role/Title of the employee
Gender	Male/Female/Other
DateOfJoining	Employee joining date
DateOfExit	If applicable, employee exit date
Salary	Monthly/Annual salary
Location	City or region
Rating	Performance rating (1 to 5)
Year	Year derived from joining or exit





New Hires = 
CALCULATE(
    COUNTROWS(EmployeeData),
    YEAR(EmployeeData[DateOfJoining]) = SELECTEDVALUE('Year'[Year])
)

Exits = 
CALCULATE(
    COUNTROWS(EmployeeData),
    NOT(ISBLANK(EmployeeData[DateOfExit])) && 
    YEAR(EmployeeData[DateOfExit]) = SELECTEDVALUE('Year'[Year])
)

Attrition Rate = DIVIDE([Exits], [Total Employees], 0)
🧠 Insights Generated
Which department has the highest employee turnover?

How does the monthly hiring rate compare to attrition?

Are there any pay disparities across departments or genders?

What is the average performance rating across years?

## 📁 Files Included
EmployeeData.csv – Sample dataset

Employee_Yearly_Analysis.pbix – Power BI Dashboard

README.md – Project documentation

📌 Tools Used
Power BI Desktop

DAX

Power Query

Excel (for data cleaning, optional)

## 📞 Contact
For questions or collaboration:
Atharva – atharvatiwari375@gmail.com
