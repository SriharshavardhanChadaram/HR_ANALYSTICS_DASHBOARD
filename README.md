# HR_Analytics_Dashboard_PowerBI

𝖨𝗇 𝗍𝗁𝗂𝗌 𝗉𝗋𝗈𝗃𝖾𝖼𝗍, 𝖨 𝗁𝖺𝗏𝖾 𝗍𝗈 𝗉𝗅𝖺𝗒 𝖺𝗇 𝖧𝖱 𝖠𝗇𝖺𝗅𝗒𝗌𝗍 𝖱𝗈𝗅𝖾 𝗍𝗈 𝖻𝗎𝗂𝗅𝖽 𝖺 𝗏𝗂𝗌𝗎𝖺𝗅𝗅𝗒 𝗂𝗆𝗆𝖾𝗋𝗌𝗂𝗏𝖾 𝗂𝗇𝗍𝖾𝗋𝖺𝖼𝗍𝗂𝗏𝖾 𝖽𝖺𝗌𝗁𝖻𝗈𝖺𝗋𝖽 𝗍𝗈 𝗎𝗇𝖽𝖾𝗋𝗌𝗍𝖺𝗇𝖽 𝗐𝗁𝗒 𝖾𝗆𝗉𝗅𝗈𝗒𝖾𝖾𝗌 𝖺𝗋𝖾 𝗅𝖾𝖺𝗏𝗂𝗇𝗀 𝗍𝗁𝖾 𝗈𝗋𝗀𝖺𝗇𝗂𝗓𝖺𝗍𝗂𝗈𝗇 𝗌𝗈 𝗍𝗁𝖺𝗍 𝗍𝗁𝖾 𝗈𝗋𝗀𝖺𝗇𝗂𝗓𝖺𝗍𝗂𝗈𝗇 𝖼𝖺𝗇 𝗎𝗇𝖽𝖾𝗋𝗌𝗍𝖺𝗇𝖽 𝗍𝗁𝖾 𝗄𝖾𝗒 𝖿𝖺𝖼𝗍𝗈𝗋𝗌 𝗋𝖾𝗀𝖺𝗋𝖽𝗂𝗇𝗀 𝖺𝗍𝗍𝗋𝗂𝗍𝗂𝗈𝗇 𝖺𝗇𝖽 𝗆𝖺𝗄𝖾 𝖽𝖺𝗍𝖺-𝖽𝗋𝗂𝗏𝖾𝗇 𝖽𝖾𝖼𝗂𝗌𝗂𝗈𝗇𝗌 𝗍𝗈 𝗋𝖾𝖽𝗎𝖼𝖾 𝗍𝗁𝖾 𝖺𝗍𝗍𝗋𝗂𝗍𝗂𝗈𝗇 𝗋𝖺𝗍𝖾 𝖻𝗒 𝗂𝗆𝗉𝗋𝗈𝗏𝗂𝗇𝗀 𝗍𝗁𝖾 𝗁𝗂𝗋𝗂𝗇𝗀 𝗉𝗋𝗈𝖼𝖾𝗌𝗌 𝖺𝗇𝖽 𝖾𝗆𝗉𝗅𝗈𝗒𝖾𝖾 𝖾𝗑𝗉𝖾𝗋𝗂𝖾𝗇𝖼𝖾 𝗍𝗁𝗎𝗌 𝗆𝖺𝗄𝗂𝗇𝗀 𝗍𝗁𝖾 𝗐𝗈𝗋𝗄𝖿𝗈𝗋𝖼𝖾 𝗆𝗈𝗋𝖾 𝗉𝗋𝗈𝖽𝗎𝖼𝗍𝗂𝗏𝖾 𝖺𝗇𝖽 𝗀𝖺𝗂𝗇 𝖾𝗆𝗉𝗅𝗈𝗒𝖾𝖾 𝗍𝗋𝗎𝗌𝗍 𝗎𝗌𝗂𝗇𝗀 𝖯𝗈𝗐𝖾𝗋 𝖡𝖨.

![Project 2 dashboard](https://github.com/CoderNitu/HR_Analytics_Dashboard_PowerBI/assets/87817227/25cf232c-87d1-472f-91ae-81f25b759656)

https://github.com/CoderNitu/HR_Analytics_Dashboard_PowerBI/assets/87817227/4214abf4-f4d8-4088-bc0e-4be22d70c6b3


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
