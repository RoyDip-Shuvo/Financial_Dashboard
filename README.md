# Financial Report Dashboard for Future-Focused Innovation Labs (FFIL) - 2023
This repository features a **Power BI Financial Analysis Dashboard** created for **Future-Focused Innovation Labs (FFIL)**. The dashboard offers key insights into revenue, expenses, and profitability for the fiscal year 2023. It visualizes critical business metrics and enables stakeholders to make informed decisions based on financial performance.

## 🛠 Tools Used:
- Power BI: Data modeling, dashboard creation, and report automation.
- DAX: Custom measures and calculations for financial analysis.
- Figma: This design tool is used for the dashboard layout and background design.
 
### [Live Dashboard](https://app.powerbi.com/view?r=eyJrIjoiZGI1YWRmMDAtMGUwNi00MjAyLTgwMWYtOWUzMjFmZjQxNDUwIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

![Navigation_page](https://github.com/RoyDip-Shuvo/Financial_Dashboard/blob/main/Images/Navigation.png)

## 🚀 Project Overview
The Financial Report Dashboard is designed to provide a comprehensive financial overview of the company’s operations. It includes key metrics such as Revenue, Expenses, Gross Profit, and Net Profit, along with detailed visualizations of how different business lines perform. The dashboard has interactive elements that allow users to filter data by month, business lines, and various financial categories.

![Overview](https://github.com/RoyDip-Shuvo/Financial_Dashboard/blob/main/Images/Overview.png)

## 📊 Data Highlights:
- Total Revenue: $17.56M
- Total Expense: $13.25M
- Gross Profit Margin: 61.78%
- Net Profit: $4.31M
- Business Line Performance: Sportswear, Sports Equipment, and Nutrition & Food Supplements performance highlighted.

![KPI Card](https://github.com/RoyDip-Shuvo/Financial_Dashboard/blob/main/Images/Git_image/KPI%20Card.jpg)

### Key Features:
### Revenue and Expense Breakdown:

- Visualizes total revenue and expense on a monthly basis.
- Highlights performance across different business lines (Sportswear, Sports Equipment, Nutrition & Food Supplements).

### Profitability Insights:

- Gross Profit (GP) and Net Profit (NP) margins displayed for key performance tracking.

### Revenue and Expense Target Comparison:

- Displays actual performance against business targets for both revenue and expenses.

### Monthly Comparisons:

- Line charts to visualize trends in revenue vs target and by business line over the months.

### Interactive Filters:

- Customizable slicers to filter data by specific months or categories for a tailored view.

![Key Feature](https://github.com/RoyDip-Shuvo/Financial_Dashboard/blob/main/Images/Git_image/Key%20Feature.jpg)

## 📈 Profit Breakdown Section
This section provides a detailed breakdown of the Operating Profit, Net Profit, COGS, and EBIT (Earnings Before Interest and Taxes) for the fiscal year 2023. It highlights performance on both a monthly and quarterly basis to offer insights into profitability trends.

## Key Visuals:

### Operating Profit Breakdown:
- Visualized by month and quarter.
- Includes Total Revenue and Gross Profit (GP) Margin for each period.

### Net Profit Breakdown:
- Tracks Net Profit and NP Margin % over time to provide a snapshot of business performance.

### COGS Breakdown:
- Details the Cost of Goods Sold (COGS) across business lines: Sports Equipment, Sportswear, and Nutrition & Food Supplements.

### EBIT & EBIT Margin %:
- Shows the Earnings Before Interest and Taxes (EBIT) for each business line with a breakdown of EBIT Margin % over the months and quarters.

![Profit_Breakdown](https://github.com/RoyDip-Shuvo/Financial_Dashboard/blob/main/Images/Git_image/Profit%20Breakdown.jpg)

Dax Code: 
```bash

```
## 📊 Expense Breakdown Section
This section provides a breakdown of the company’s expenses, including COGS, OPEX (Operating Expenses), and Interest & Tax for the fiscal year 2023. It offers insights into where the company is spending across different categories and business lines.

## Key Visuals:

### Monthly Breakdown of COGS, OPEX, and Interest & Tax:
- A stacked bar chart representing monthly expense distribution across these categories.

### Expense Breakdown by Business Line:
- Shows how each business line (Nutrition & Food Supplements, Sports Equipment, and Sportswear) contributes to total expenses.

### OPEX Breakdown:
- Divided into equipment, marketing, payroll, R&D, rent, and other subcategories, with a detailed look at each business line.

### COGS Breakdown:
- Focused on labor, materials, and other production-related costs for each business line.

### Interest & Tax Breakdown:
- Displays the allocation of interest and tax expenses by business line.
  
![ExpenseBreakdown](https://github.com/RoyDip-Shuvo/Financial_Dashboard/blob/main/Images/Git_image/Expense%20Breakdown.jpg)

Dax code:
```bash
```

## 📊 Income & Expense Statements
This section presents a Quarterly Income and Expense Statement for the year 2023. It provides a breakdown of revenue, expenses, and quarterly-over-quarter analysis (QoQ) across different business lines.

### Key Features:
### Quarterly Revenue & Expense Data:
- Breakdown by business lines: Nutrition & Food Supplements, Sports Equipment, and Sportswear.

### QoQ Performance:
- Highlights the percentage growth or decline quarter-over-quarter for each business line and cost category.

### Income Statement:
- Displays revenue from various sources, such as consulting services, other income, and sales.

### Expense Statement:
- Details costs associated with COGS, Opex, and interest/tax.

![Income_Expense_Statement](https://github.com/RoyDip-Shuvo/Financial_Dashboard/blob/main/Images/Income_Expense%20Statement.png)


Dax Code: 
```bash
-----------------------------------------------------------------------------------------------------

QoQ△ = 
 Var PQ_Rev = CALCULATE([Total Revenue], DATEADD('Date'[Date],-1,QUARTER))
 VAR Current_Rev = [Total Revenue]
 VAR Result = Current_Rev - PQ_Rev
 RETURN
 Result

-----------------------------------------------------------------------------------------------------

QoQ△% = DIVIDE([QoQ△],[Total Revenue])

-----------------------------------------------------------------------------------------------------

EXP QoQ△ = 
VAR PQ = CALCULATE([Total Expense], DATEADD('Date'[Date], -1, QUARTER))
VAR Curent = [Total Expense]
VAR Result = Curent - pq
RETURN
Result

-----------------------------------------------------------------------------------------------------

EXP QoQ△% = DIVIDE([EXP QoQ△], [Total Expense])

-----------------------------------------------------------------------------------------------------
```


