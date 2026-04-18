# 🛒 Retail Orders — Multi-Region Sales Analysis

**Dataset:** Orders data across Central, East & West regions | **Tool:** R

## Overview
Joined and cleaned three regional retail order datasets from different formats (CSV and tab-delimited) to answer 6+ business questions about shipping performance, profit, and customer behaviour across a retail chain.

## 🎯 Key Business Questions Answered

| Question | Approach |
|---|---|
| Which region ships fastest on average? | Computed `mean(Ship.Date - Order.Date)` per region |
| Which products ship slowest by region? | Grouped by Region + Product, filtered max shipping time |
| Time to ship by category and year | ggplot2 bar chart with category fill |
| Highest profit categories by region | `aggregate(Profit ~ Region + Category)` |
| Segments with lowest profit by region | `group_by + summarise + slice_head` |
| Yearly sales by region | `mutate(Year) + group_by + summarise` |
| Highest-spending customer store-wide & by region | `group_by + summarise + filter(max)` |

## 🛠️ Tech Stack
- **Language:** R
- **Libraries:** `dplyr`, `tidyr`, `tidyverse`, `ggplot2`
- **Data:** `Orders_Central.csv`, `orders_west.csv`, `Orders_East.txt` (tab-separated)

## 🔍 Methodology
1. Loaded 3 datasets with different formats and date structures
2. Standardised date columns across all three regions
3. Removed missing values and aligned column names
4. Combined with `rbind()` after adding Region column
5. Answered each business question using `dplyr` pipelines
6. Visualised shipping time by category/year with `ggplot2`

## 💡 What I Learned
Real-world data never arrives in a single clean file. This project taught me how to merge datasets with different formats, standardise inconsistent date fields, and build reusable analysis pipelines. The business questions mirror exactly what a retail BI analyst faces day-to-day.

---
*Part of my data analytics portfolio — [view all projects](https://github.com/Jahnavi0605)*
