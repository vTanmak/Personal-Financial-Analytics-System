# Personal Financial Analytics System

A personal finance dashboard built in Microsoft Power BI that brings together income, expenses, budget tracking, and savings data into a single interactive report. The goal was to go beyond basic charts and build something that actually helps users understand their financial situation and plan ahead.

---

## What it covers

The report has five pages, each focused on a different aspect of personal finance:

- **Financial Overview** — High-level KPIs (Total Income, Total Expenses, Net Savings, Savings Rate) with trend and area charts showing how income and expenses moved across the year.
- **Expense Intelligence** — A detailed breakdown of spending by category, a budget vs. actual comparison table with colour-coded status, and a day-of-week spending pattern analysis.
- **Smart Insights** — Four auto-generated text cards that produce readable sentences from the data, such as weekend vs. weekday spending differences and month-on-month changes. These update automatically when filters change.
- **Savings Forecast** — A What-If parameter slider that lets you simulate a change in expense levels (from -50% to +50%) and instantly see the effect on predicted savings. Includes a 3-month moving average trend chart.
- **Financial Health Score** — A composite score out of 100 based on three factors: Savings Rate (40 pts), Budget Control (35 pts), and Spending Stability (25 pts). Displayed as a gauge with a component breakdown.

---

## Data Model

The report uses a **Star Schema** with four tables:

| Table | Role |
|---|---|
| Transactions | Fact table with income/expense records |
| Calendar | Date dimension with Month, Quarter, Year, etc. |
| Categories | Bridge table linking Transactions and Budget |
| Budget | Monthly budget targets per category |

---

## Tech Stack

- Microsoft Power BI Desktop
- DAX (custom measures)
- Power Query (M Language)
- CSV flat files as data source

---

## Files

```
├── Project.pbix                          # Power BI report file
├── DataSet/                              # CSV data files
│   ├── Transactions.csv
│   ├── Budget.csv
│   └── Categories.csv
└── 23051635_Tanishq Makhija_Power BI Report.pdf   # Submitted documentation
```

---

## Key Features

- Dynamic text insights generated entirely in DAX with no external tools
- What-If scenario analysis using Power BI parameters
- Composite financial health scoring across three dimensions
- Slicers synced across all five pages for seamless navigation
- Conditional formatting on budget table driven by DAX logic

---

**Name:** Tanishq Makhija  
**Roll Number:** 23051635  
**Program:** B.Tech CSE
