# 05. Advanced Distribution Analytics & Root Cause Diagnosis

Combining **Numeric Distribution (ND)** and **Weighted Distribution (WD)** enables diagnostics on GTM quality, channel efficiency, and sell-out performance.

---

## 1. Derived Ratios

### A. Distribution Efficiency Ratio (Quality Index)
$$\text{Efficiency Ratio} = \frac{\text{WD (\%)}}{\text{ND (\%)}}$$
* **Ratio > 1.0:** High efficiency; listings are concentrated in high-volume retail outlets.
* **Ratio < 1.0:** Low efficiency; listings are scattered across low-volume doors.

### B. Fair Share Gap
$$\text{Fair Share Gap} = \text{WD (\%)} - \text{ND (\%)}$$
* **Negative Gap (ND > WD):** Indicates missing listings in major Key Account chains.

---

## 2. Root Cause Analysis: High Distribution (ND/WD 95%) but Low Value Share

When a SKU achieves ~95% ND and ~95% WD but generates low revenue share, physical listing is solved, but velocity is constrained.

```
                  ┌─► [1] Execution & In-Store Visibility
                  │   ├── Ghost Inventory / Virtual OOS
                  │   └── Suboptimal Shelf Placement (Bottom Shelf)
                  │
HIGH ND/WD (95%) ─┼─► [2] Pricing & Pull Demand
LOW VALUE SHARE   │   ├── Uncompetitive Price Index
                  │   └── Insufficient Marketing & Consumer Pull
                  │
                  └─► [3] Portfolio Role
                      └── Niche / Specialty SKU (Inherently Low Volume)
```

### Action Plan Checklist
1. **Audit Shelf Facings (Share of Shelf):** Verify if facing ratio matches category market share.
2. **Check Store-Level On-Hand Inventories:** Identify ghost inventory holding back replenishment orders.
3. **Analyze Velocity (Sales / Store / Week):** Determine if price elasticities or promotional frequencies require adjustment.