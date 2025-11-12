# Tableau-HDFC-Project
HDFC Bank Tableau Capstone — Branch, Customer &amp; Transaction analysis
# Tableau Capstone Project – HDFC Bank Dashboards

## Project Summary
Interactive Tableau dashboards analyzing HDFC Bank customer, transaction and branch data.  
The dashboards provide insights into branch profitability, customer segmentation, transaction & investment trends to support operational and strategic decision-making.

## Tableau Public Link
Final workbook published to Tableau Public:  
<https://public.tableau.com/app/profile/muhammed.razin.v/viz/hdfcbankdata_17629468986570/HDFC?publish=yes>


## Key Insights
- Top performing branches (by revenue/profit) are concentrated in the South and West regions.  
- Business customers hold a significant portion of total investments and balances.  
- Investment volumes show a seasonal uptick mid-year; transaction volumes peak in Q2.

## Features Used
- LOD Expression(s) — e.g. `{ FIXED [Customer ID] : SUM([Transaction_Amount]) }`  
- Parameters — Top N, Measure Switch (Revenue / Profit / Expense)  
- Dashboard Actions — filter, highlight, navigation  
- Table Calculations — RANK_DENSE for Top N logic  
- Story Page — 4 story points summarizing insights

## Repository Contents
- `data/` — raw dataset(s) used (Excel/CSV)  
- `docs/` — DAD, BRD, FRD PDFs and other documentation  
- `tableau_workbook/` — `.twbx` workbook files (draft & final)  
- `screenshots/` — dashboard screenshots used in README

## How to reproduce
1. Open `tableau_workbook/final_dashboard.twbx` in Tableau Desktop or Tableau Public.  
2. Connect to the `data/raw_data.xlsx` file in the `data/` folder.  
3. All calculated fields, parameters and filters are saved in the workbook.

## Deliverables
- `final_dashboard.twbx` — Final Tableau workbook  
- `DAD.pdf`, `BRD.pdf`, `FRD.pdf` — Day-1 documentation (in `docs/`)  
- `screenshots/` — dashboard images for README and report  
- GitHub commit history showing daily commits

## Key Calculations (examples)
- **Profit Margin**: `(SUM([Revenue]) - SUM([Expenses])) / SUM([Revenue]) * 100`  
- **Customer Balance (LOD)**: `{ FIXED [Customer_ID] : SUM([Account_Balance]) }`  
- **Top N filter**: `RANK_DENSE(SUM([Revenue]), 'desc') <= [Top N]`

## Author
Razi — Data Analyst Student

---

### License
This repository is for academic/project use. Replace with an appropriate license if required.
