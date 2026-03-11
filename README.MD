# Superstore Profit Optimization Analysis 🚀
![Image Alt](https://github.com/riyabisht18/Superstore-Profit-Optimization-Analysis-/blob/860218f6e7b2e09a3a237cad82f7c65e83b4d021/Dashboard_Image.png). 

# Superstore Profit Optimization

**Objective:** Identify profit margin leakage (currently 12.5%) and model a solution to achieve 20% margin.

**Result:** Analysis of 5,009 transactions reveals that discounts exceeding 20% generate losses. Capping discounts at 20% projects a profit increase of $177,000 (+62%).

---

## Executive Summary

| Metric | Current State | Projected State | Impact |
|--------|---------------|-----------------|--------|
| **Profit** | $287K | $464K | +$177K |
| **Margin** | 12.5% | 20.2% | Target Met |
| **Discount Cap** | None | 20% Max | Policy Change |

**Key Finding:** Deep discounts (>20%) currently bleed $135,000 annually.

---

## Analysis: The 20% Profit Cliff

Transactions were grouped by discount percentage to identify profitability thresholds:

| Discount Level | Profit Impact | Margin Status |
|----------------|---------------|---------------|
| No Discount (0%) | +$321,000 | 29.5% (Strong) |
| Low (1-10%) | +$9,000 | 16.6% (Good) |
| Medium (11-20%) | +$92,000 | 11.6% (Acceptable) |
| High (21-30%) | -$10,000 | -10.0% (Loss) |
| Very High (>30%) | -$125,000 | -48.0% (Major Loss) |

**Critical Threshold:** Profitability turns negative once discounts exceed 20%. Orders with >30% discounts lose $0.48 for every $1.00 in sales.

---

## Customer Segmentation

RFM (Recency, Frequency, Monetary) analysis categorizes the customer base:

- **Loyal & Champion Segments:** 59% of customers
  - High purchase frequency and monetary value
  - Indicate product loyalty independent of deep discounting
- **Other Segments:** 41% (At Risk, New, Lost)

**Strategic Note:** The majority customer base demonstrates repeat purchase behavior, suggesting tolerance for reduced discounting, though monitoring is recommended.

---

## Recommendation

**Implement a 20% Maximum Discount Cap**

**Financial Impact:**
- Eliminates $135,000 in annual losses
- Increases net profit to $464,000 (+62%)
- Zero implementation cost (policy change only)

**How to Apply This:**
- First: Test this in Texas and Ohio only (these states lose the most money)
- Check: Wait 30 days and see if too many customers leave
- Then: If profit goes up, apply to all other states

---

## Technical Approach

- **SQL Server:** 
  - Aggregate functions (GROUP BY, SUM, COUNT) for discount tier analysis
  - CASE statements for profit categorization
  - CTEs for RFM scoring
- **Tableau:** Visualization of profit waterfalls, geographic loss mapping, and executive dashboard

---

## Repository Files

- `Superstore_Analysis_Full.sql` - Complete SQL query set (data exploration, discount analysis, RFM segmentation)
- `Superstore_Dashboard.twbx` - Tableau workbook with visualizations
- `dashboard_screenshot.png` - Executive dashboard image
- `README.md` - Project documentation

---

## Conclusion

This analysis demonstrates how fundamental SQL aggregation (GROUP BY, CASE statements) can expose critical business thresholds. Identifying the exact discount limit where profitability inverts (20%) enables a zero-cost policy intervention that recovers $177,000 in annual profit.

---

*Dataset: Sample Superstore (public dataset used for analytical practice)*


