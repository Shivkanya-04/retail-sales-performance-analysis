# Retail Sales Performance & Profitability Diagnostic  
**SQL + Power BI**

---

## Objective

This project analyzes a multi-year retail dataset to diagnose revenue performance, margin compression, and operational efficiency. The objective was to move beyond basic dashboards and uncover structural profitability risks using SQL transformations and Power BI visualization.

---

## Technical Architecture

**Database Layer:** MySQL  
**Visualization Layer:** Power BI  

### Workflow:
1. Imported raw CSV into MySQL
2. Standardized inconsistent date formats using conditional parsing
3. Created derived metrics:
   - `delivery_days`
   - `profit_margin`
   - `order_month`
4. Built analytical views for KPI and profitability diagnostics
5. Exported structured dataset into Power BI
6. Designed a 3-page consulting-style dashboard

---

## Data Preparation (SQL)

Key transformations:
- Conditional date parsing using `STR_TO_DATE`
- Created `delivery_days = ship_date - order_date`
- Computed `profit_margin = profit / sales`
- Created monthly aggregation key for trend analysis
- Grouped discount buckets (0–10%, 10–20%, 20%+)

All transformations were performed in SQL before visualization to ensure analytical integrity.

---

## Key Business Insights

### Overall Performance
- **Total Revenue:** $2.29M  
- **Total Profit:** $286K  
- **Profit Margin:** 12.47%  
- Strong Q4 seasonality observed annually

---

### Margin Compression Identified

| Category | Revenue | Margin |
|----------|----------|--------|
| Furniture | $742K | 2.49% |
| Office Supplies | $719K | 17.04% |
| Technology | $836K | 17.40% |

Furniture significantly drags overall profitability.

---

### Loss-Making Sub-Categories

- Tables → -8.56% margin  
- Bookcases → -3.02% margin  
- Supplies → -2.55% margin  

High revenue does not guarantee profitability.

---

### Discount Impact

| Discount Bucket | Margin |
|----------------|--------|
| 0–10% | 28.89% |
| 10–20% | 11.58% |
| 20%+ | -37.32% |

Discounting beyond 20% results in severe margin erosion.

---

### Shipping Analysis

- Shipping speed has minimal margin impact (12–14% range)
- Standard Class dominates revenue (~59%)

Operational cost-to-serve is not the primary margin driver. Pricing strategy is.

---

## Dashboard Structure

### Page 1 — Executive Overview
- KPI cards
- Monthly revenue trend
- Revenue by category & segment

### Page 2 — Margin Risk & Product Optimization
- Loss-making sub-categories
- Discount impact visualization
- Category margin comparison

### Page 3 — Operational & Regional Insights
- Shipping mode performance
- Regional revenue distribution
- Revenue vs Profit scatter analysis

---

## Skills Demonstrated

- SQL data modeling
- Data cleaning & transformation
- KPI construction
- Profitability diagnostics
- Business insight generation
- Data storytelling through visualization

---

Data Source: This project uses a publicly available retail dataset commonly used for analytics practice and business intelligence case studies.

---

## Conclusion

This project demonstrates how structured SQL transformation combined with BI visualization can uncover structural profitability issues and support data-driven decision-making.
