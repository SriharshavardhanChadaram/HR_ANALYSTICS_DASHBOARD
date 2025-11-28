
# 👨‍💼 HR Analytics Dashboard – Power BI (GitHub Version)

## 📌 Overview
The **HR Analytics Dashboard** provides insights into employee retention, absenteeism, department performance, attrition, and workforce trends.  
Built using **Power BI, DAX, Power Query, and Python**, this project showcases end-to-end analytics workflow and dashboard development.

---

## ⭐ Key Features
- Workforce Overview (Headcount, Attrition, Hiring)
- Employee Tenure Analysis
- Attendance & Absenteeism Insights
- Department Performance Comparison
- Attrition Drivers + Risk Indicators
- Fully Automated ETL Pipeline (Power Query & Python)

---

## 🛠 Tech Stack
- **Power BI Desktop**
- **Power Query (M Language)**
- **DAX**
- **Python (Pandas)**
- **Excel CSV Data Sources**

---

## 📁 Folder Structure
```
HR_Analytics_GitHub_Project/
│── data/               → Employee & Attendance datasets
│── scripts/            → Python ETL script
│── dax/                → DAX measures for Power BI
│── powerquery/         → M scripts for transformations
│── report_layout/      → Dashboard design guide
│── theme/              → Power BI JSON theme
│── images/             → Banner + Dashboard images
│── README.md           → Project documentation
```

---

## 🔢 DAX Measures (Examples)
```DAX
Total Employees = DISTINCTCOUNT(Employee[EmpID])

Attrition Count =
CALCULATE(COUNT(Employee[EmpID]), Employee[Status] = "Left")

Attrition Rate =
DIVIDE([Attrition Count], [Total Employees], 0)

Average Tenure =
AVERAGEX(Employee, DATEDIFF(Employee[JoinDate], TODAY(), YEAR))
```

---

## 🔧 Power Query M (ETL)
```M
let
    EmpSource = Csv.Document(File.Contents("employee_data.csv"),[Delimiter=",", Encoding=1252]),
    EmpHeaders = Table.PromoteHeaders(EmpSource),
    EmpTypes = Table.TransformColumnTypes(EmpHeaders,{{"EmpID", Int64.Type}, {"JoinDate", type date}}),

    AttSource = Csv.Document(File.Contents("attendance.csv"),[Delimiter=",", Encoding=1252]),
    AttHeaders = Table.PromoteHeaders(AttSource),
    AttTypes = Table.TransformColumnTypes(AttHeaders,{{"EmpID", Int64.Type}, {"Date", type date}}),

    AddedAbsent = Table.AddColumn(AttTypes, "Absent", each if [Status]="Absent" then 1 else 0),
    Merged = Table.NestedJoin(EmpTypes, {"EmpID"}, AddedAbsent, {"EmpID"}, "Attendance"),
    Expanded = Table.ExpandTableColumn(Merged, "Attendance", {"Date","Status","Absent"})
in
    Expanded
```

---

## 📊 Dashboard Pages
### **Page 1 — HR Overview**
- KPIs: Headcount, Attrition Rate, Avg Tenure  
- Department-wise headcount  
- Workforce trend line chart  

### **Page 2 — Attendance Insights**
- Absenteeism heatmap  
- Dept-wise absenteeism chart  
- Daily/Monthly attendance trends  

### **Page 3 — Attrition Analysis**
- Active vs Left breakdown  
- Tenure of employees who left  
- Potential attrition causes  

---

## 📷 Dashboard Preview
(Add your dashboard screenshots inside `/images/`)

---

## 📬 Contact
**Author:** Sri Harsha Vardhan  
📧 Email: your-email@example.com  
🔗 GitHub: https://github.com/  

---

## ⭐ Support
If you like this project, please ⭐ star the repository!
