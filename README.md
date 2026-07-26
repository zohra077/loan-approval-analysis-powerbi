# loan-approval-analysis-powerbi
Interactive Power BI dashboard analyzing loan approval trends, applicant demographics, and key financial metrics using DAX, Power Query, and data visualization.
# 📊 Loan Approval Analysis Dashboard (Power BI)

## 📌 Project Overview
This project is an interactive **Loan Approval Analysis Dashboard** developed using **Microsoft Power BI**. The dashboard provides valuable insights into loan applications, approvals, applicant income, loan amounts, and demographic trends. It helps financial institutions understand approval patterns and supports data-driven decision-making.

---

## 🎯 Objectives
- Analyze loan application data.
- Track loan approval and rejection rates.
- Understand applicant demographics.
- Identify factors influencing loan approvals.
- Visualize key business metrics using interactive dashboards.

---

## 🛠️ Tools & Technologies
- Microsoft Power BI
- Power Query
- DAX (Data Analysis Expressions)
- CSV Dataset
- Data Cleaning & Transformation

---

## 📂 Dataset Information
The dataset contains information about loan applicants, including:

- Loan ID
- Gender
- Marital Status
- Dependents
- Education
- Self Employed
- Applicant Income
- Coapplicant Income
- Loan Amount
- Loan Amount Term
- Credit History
- Property Area
- Loan Status

---

## 🧹 Data Cleaning Process
The following preprocessing steps were performed:

- Removed duplicate records
- Handled missing values
- Corrected data types
- Renamed columns for consistency
- Verified data quality
- Loaded cleaned data into Power BI

---

## 📈 DAX Measures Created

### Total Applications
```DAX
Total Applications = COUNT(LoanData[Loan_ID])
```

### Approved Loans
```DAX
Approved Loans =
CALCULATE(
COUNT(LoanData[Loan_ID]),
LoanData[Loan_Status]="Y"
)
```

### Rejected Loans
```DAX
Rejected Loans =
CALCULATE(
COUNT(LoanData[Loan_ID]),
LoanData[Loan_Status]="N"
)
```

### Approval Rate
```DAX
Approval Rate =
DIVIDE(
[Approved Loans],
[Total Applications],
0
)
```

### Average Loan Amount
```DAX
Average Loan Amount =
AVERAGE(LoanData[LoanAmount])
```

### Average Applicant Income
```DAX
Average Applicant Income =
AVERAGE(LoanData[ApplicantIncome])
```

### Average Coapplicant Income
```DAX
Average Coapplicant Income =
AVERAGE(LoanData[CoapplicantIncome])
```

---

## 📊 Dashboard Features

The dashboard includes:

- KPI Cards
  - Total Applications
  - Approved Loans
  - Rejected Loans
  - Approval Rate
  - Average Loan Amount
  - Average Applicant Income
  - Average Coapplicant Income

- Loan Approval by Gender

- Loan Approval by Education

- Loan Approval by Property Area

- Loan Approval by Marital Status

- Loan Approval by Credit History

- Applicant Income Analysis

- Interactive Filters (Slicers)

---

## 📷 Dashboard Preview

> *(Add screenshots of your dashboard here after uploading them.)*

Example:

```
Dashboard_Screenshot.png
```

---

## 📌 Key Insights

- Applicants with a positive credit history have significantly higher approval rates.
- Urban and Semi-Urban applicants receive more loan approvals.
- Graduate applicants show a slightly better approval percentage.
- Applicant income positively influences loan approval.
- Interactive filters allow dynamic exploration of the data.

---

## 🚀 How to Use

1. Download the `.pbix` file.
2. Open it in **Microsoft Power BI Desktop**.
3. Refresh the dataset if required.
4. Explore the dashboard using slicers and filters.

---

## 📁 Repository Structure

```
Loan-Approval-Analysis/
│
├── LoanApprovalDashboard.pbix
├── LoanData.csv
├── Dashboard_Screenshot.png
├── README.md
└── LICENSE
```

---

## 💡 Skills Demonstrated

- Data Cleaning
- Data Transformation
- Data Modeling
- DAX
- Power BI Dashboard Design
- Business Intelligence
- Data Visualization
- Analytical Thinking

---

## 📬 Contact

**Fatimuz Zohra**

GitHub: https://github.com/yourusername

LinkedIn: https://linkedin.com/in/yourprofile

---

## ⭐ If you found this project useful, consider giving it a Star!
