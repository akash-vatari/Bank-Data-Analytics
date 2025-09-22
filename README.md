# Bank-Data-Analytics
Bank Data Analysis – Performed data cleaning, analysis, and visualization using SQL, Excel, Power BI, and Tableau to uncover key banking insights.
This project focuses on analyzing banking and loan data using Excel, SQL, Tableau, and Power BI.
The goal is to generate actionable insights for stakeholders on loan performance, repayment trends, delinquency, and branch-wise performance.

🛠 Tools & Technologies

Excel → Data cleaning, preprocessing, and initial dashboarding

SQL (MySQL) → Data storage, queries, and transformations

Power BI → Interactive loan analytics dashboard

Tableau → Advanced visual analytics and storytelling

📂 Dataset
https://drive.google.com/drive/folders/1aZZ0Lp6rEbENIUnQQ8d9INKYU4P7VjwF?usp=drive_link

The dataset contains loan-related records with attributes such as:

Client details (Client ID, Age, Gender, Religion, etc.)

Loan details (Loan ID, Loan Amount, Term, Interest Rate, Product, Status)

Repayment details (Total Payment, Principal, Interest, Fees, Recoveries)

Branch & State information

Flags (Is Delinquent Loan, Is Default Loan, Verification Status)

⚠ Note: Sensitive personal information was removed/kept anonymized for analysis.

📊 Key Metrics (KPIs)

Total Loan Amount Funded → Total value of loans disbursed

Total Loans Issued → Number of loans (Active, Closed, Defaulted)

Total Collection → Principal + Interest + Fees collected

Total Interest Earned → Revenue from interest payments

Branch-wise & State-wise Loan Performance

Disbursement Trend Over Time

Grade-wise Loan Risk Profile

Default Loan Count & Default Loan Rate

Delinquent Client Count & Delinquent Loan Rate

Age Group-wise Loan Distribution

Product Group-wise Loan Analysis

Loan Status Overview (Active, Closed, Default, Delinquent)

🧮 Example Calculations

Delinquent Loan Rate (Tableau):

SUM( IF [Is Delinquent Loan] = "Y" THEN 1 ELSE 0 END ) / COUNT([Loan ID])


Default Loan Count (Power BI - DAX):

Default Loan Count =
COUNTROWS (
    FILTER (
        'LoanData',
        'LoanData'[Is Default Loan] = "Y"
    )
)


Total Collection (Tableau):

SUM([Total Rec Prncp]) + SUM([Total Rrec int]) + SUM([Total Fees])

📑 Project Workflow

Excel → Cleaned and pre-processed raw data, created preliminary dashboard.

SQL → Loaded data into database, ran queries for validation & aggregation.

Power BI → Built interactive loan analytics dashboard with KPIs and filters.

Tableau → Designed advanced visual dashboards for storytelling.

Final Output → Compared results across tools to ensure accuracy.

📷 Dashboard Snapshots

https://drive.google.com/drive/folders/1gtBoHltXGdasojvSlphbmAf7_MwVJpPT?usp=drive_link

🚀 Key Insights

Identified high default risk groups based on age and grade.

Monitored state and branch performance to detect underperforming regions.

Tracked repayment efficiency and highlighted delinquent clients.

Visualized disbursement trends, showing growth patterns in lending.

📌 Future Improvements

Automate ETL pipelines for real-time data refresh.

Integrate predictive modeling for loan default risk.

Deploy dashboards to cloud platforms for wider accessibility.
