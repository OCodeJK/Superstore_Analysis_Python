# Superstore Sales EDA
![Profit Margin by Discount Level](insights/discount_margin_chart.png)

## Overview
An exploratory data analysis of the Sample Superstore dataset containing 9,994 
retail orders across the United States. The goal was to identify what is driving 
profit losses across products, regions and customer segments.

The analysis uncovered a single root cause threading through every section: 
**excessive discounting above 20% is systematically destroying profitability** 
across specific products, states and regions.

---

## Tools Used
- Python 3
- Pandas — data cleaning and aggregation
- Matplotlib & Seaborn — data visualization
- Jupyter Notebook — analysis environment

---

## Dataset
- **Source:** Sample Superstore Dataset (Kaggle)
- **Rows:** 9,994 orders
- **Columns:** 19 (Sales, Profit, Discount, Quantity, Category, Region, State, Segment etc.)
- **Date Range:** 2014 — 2017

---

## Key Findings

### 1. Profitability by Product
- Technology is the most profitable category at 17.4% margin
- Furniture is severely underperforming at only 2.49% margin despite 
  $741,999 in sales
- 3 sub-categories are actively losing money: Tables (-$17,725), 
  Bookcases (-$3,472) and Supplies (-$1,189)
- Tables is the most alarming — 4th highest selling sub-category yet 
  the largest loss-maker in the entire dataset

### 2. Profitability by Region & State
- West is the strongest region at 14.94% margin
- Central is the weakest at 7.92% — less than half of West's margin
- Texas is the most critical state: 3rd highest sales ($170k) yet 
  loses -$25,729 at a -15.12% margin
- All 10 bottom states by profit are loss-making

### 3. Discount vs Profit — The Core Finding
- Orders with 0% discount average a 29.51% profit margin
- The tipping point is exactly at 20% — every order discounted 
  above 20% loses money without exception
- Orders discounted 50%+ have a -119% margin
- Discount vs Sales correlation is only -0.03 — discounting is not 
  even driving more sales, making it pure margin destruction

### 4. Customer Segments
- Home Office is the most profitable segment at 14.03% margin with 
  the highest average order value ($240.97)
- Consumer is the largest segment ($1.16M) but least efficient at 11.55% margin

---

## Recommendations
1. **Cap discounts at 20%** — all orders above this threshold lose money 
   without generating meaningfully more sales volume
2. **Review Tables sub-category pricing** — $17,725 in losses despite high 
   sales volume suggests a fundamental pricing or cost structure problem
3. **Investigate Central region and key states** (Texas, Ohio, Pennsylvania) 
   — apply discount cap and monitor margin recovery

---

## Visualizations
The notebook contains the following charts:
- Sales vs Profit by Category (grouped bar chart)
- Profit by Sub-Category (horizontal bar chart with negative bars highlighted)
- Sales vs Profit by Region (grouped bar chart)
- Top 10 and Bottom 10 States by Profit (side by side horizontal bar charts)
- Sales vs Profit by Segment (grouped bar chart)
- Discount vs Profit (scatter plot)
- Average Profit Margin by Discount Level (bar chart)
- Correlation Matrix (heatmap)

---

## How to Run
1. Clone this repository
2. Download the dataset from this repo (Superstore_Sample.csv)
3. Place the CSV in your work folder
4. Open `notebooks/superstore_eda.ipynb` in Jupyter Notebook
5. Run all cells from top to bottom

---

## Related Projects
- [[Northwind Sales Analytics](https://github.com/OCodeJK/northwind_analysis_sql)] — SQL-based sales 
  analysis using PostgreSQL and DBeaver
