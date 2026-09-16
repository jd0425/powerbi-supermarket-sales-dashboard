# Power BI — Supermarket Sales Dashboard

A Power BI report analyzing supermarket sales performance across branches, product lines, payment types, and customer segments. Built as a portfolio piece to demonstrate data modeling, DAX measures, and interactive report design in Power BI.

## Contents

- `Supermarket-Sales-Dashboard.pbix` — the Power BI report file (open in Power BI Desktop or upload to Power BI Service to explore)

## Data Model

The report is built on a star schema:

- **Fact table:** `Sales Data` — individual sales transactions (totals, gross income, quantity, ratings, order counts)
- **Dimension tables:**
  - `DIM_Date` — Year, Quarter, Month Name, Date
  - `DIM_ProdLine` — Product line
  - `DIM_CityBranch` — City, Branch, City (Branch)
  - `DIM_Payment` — Payment method
  - `DIM_Gender` — Customer gender
  - `DIM_CustomerType` — Customer type

## Measures

The report uses several DAX measures (defined in `Calc` / `Calcs` measure tables), referenced across the visuals:

- `Total Sales`
- `Total Quantity Sold`
- `MOM % Change` (month-over-month change)
- `Refresh date`

> Note: the DAX formulas themselves aren't included yet — Power BI stores the compiled data model in a compressed binary format that isn't readable outside Power BI Desktop / Tabular Editor. Opening the `.pbix` file directly shows the full measure definitions.

## Report Pages

**1. PBI Sales Dashboard** — the main dashboard, including:
- KPI cards: total orders, total sales, total quantity sold, average rating, last refresh date
- Clustered bar chart — Sales by Product Line
- Ribbon chart — Total Gross Income by month/quarter
- Donut chart — Total Sales by City (Branch)
- Column chart — Total Sales by Payment Type (segmented by gender and branch)
- Slicers for Date, City/Branch, Product Line, Payment, Gender, and Customer Type

**2. Supporting Table View** — detail tables for drill-down analysis:
- Monthly sales summary table (Year, Month, Orders, Gross Income, Total Sales, MOM % Change)
- Branch/product line breakdown table
- Matching KPI cards and slicers for consistent filtering

## Tools & Skills Demonstrated

- Power BI report design (cards, bar/column/donut/ribbon charts, tables, slicers, cross-filtering)
- Star-schema data modeling
- DAX measures for aggregation and time-based calculations
- Custom report theming/branding

## Viewing the Report

Power BI Desktop is Windows-only. To view this report:
- **Windows:** open the `.pbix` file directly in [Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads) (free)
- **Mac/any OS:** upload the `.pbix` file to the [Power BI Service](https://app.powerbi.com) (free account) and open it in the browser

---
*Screenshots and full DAX formula listings to be added.*
