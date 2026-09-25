# 🏖️ Beach Bar Seasonal Analytics

**A self-directed data analytics project** (Summer 2025) analyzing seasonal
sales data for a beach bar business — an end-to-end SQL →
Excel → Power BI workflow.

---

## 🎯 Objective

> Does the data support raising sunbed prices on peak-season weekends
> (July–August), and what else in the operation deserves attention?

---

## 📊 Data

| | |
|---|---|
| **Period** | May – September 2025 (153 days) |
| **Scope** | Sunbed occupancy, 21 menu products (8 categories), revenue by 4 daily time windows |
| **Source** | Real sales data from a beach bar business, provided to me by an acquaintance/owner of the business for academic coursework purposes.
---

## 🛠️ Method

| Tool | Role |
|---|---|
| **SQL** (`beachbar_analysis.sql`) | 6 queries — monthly summary, weekday/weekend capacity check, top products, a stock-out investigation, time-of-day breakdown, price scenario. Self-contained: schema + data + queries in one file, runs standalone in SQLite. |
| **Excel** (`beachbar_analysis.xlsx`) | Formula-driven summary workbook — Overview + 4 sheets, no hardcoded values. |
| **Power BI** | 4-page interactive dashboard — Overview, Capacity & Pricing, Products, Time of Day. |

---

## 📈 Key results

| Metric | Value |
|---|---|
| Total revenue (season) | **€111,342.5** |
| Average occupancy | **74.4%** |
| Peak-season weekend occupancy | **94.4%** (vs. 83.4% weekday) |
| Top product | **Draft Beer** (€7,530) |
| Weakest time window | **18:00–21:00** (€12,152) |
| +5% price scenario | +€1,822 (sunbeds), +€3,746 (F&B) — assumes unchanged volume |

---

## 🔍 Findings

1. **Capacity is the real constraint, not overall demand.** Only July–August
   weekends run near full capacity (93–96%); every other period has spare
   capacity — a season-wide price increase isn't supported by the data.
2. **A 10-day zero-revenue gap in Mojito sales** (Aug 10–19) was investigated
   and traced to a supply stock-out, not falling demand — substitute
   cocktails (Aperol Spritz, Margarita) absorbed the volume in the same
   window.
3. **Evening hours underperform consistently.** 18:00–21:00 is the weakest
   revenue window — a candidate for targeted promotions or staffing review.

---

## ✅ Recommendation

Test a price increase on **peak weekends only**, not season-wide — the
capacity data doesn't support broader change. Track weekend occupancy
against the 94.4% historical baseline during the test period before rolling
out any permanent change.

---

## 🧪 Quality check

The SQL was reviewed for join correctness, GROUP BY logic, cross-dialect
portability, and unsafe statements; findings were fixed and results
re-verified as unchanged after the fixes.

---

## ⚠️ Limitations

The data is real, but price was never historically varied — so demand elasticity cannot be estimated from it. The +5% figure is a working scenario, not a forecast
