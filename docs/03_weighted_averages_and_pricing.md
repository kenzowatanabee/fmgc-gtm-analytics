# 03. Weighted Averages vs. Averages of Averages

A common pitfall in revenue analytics is calculating the simple arithmetic mean of monthly prices or averages across groups with unequal volumes.

---

## 1. Why "Averages of Averages" Fails

When group sizes differ, taking a simple average of group averages ignores the relative weight of each group, skewing the overall metric.

### Example: School Class Averages
* **Class A (Small):** 2 students with score **10** $\rightarrow$ Mean = **10**
* **Class B (Large):** 98 students with score **0** $\rightarrow$ Mean = **0**

$$\text{Incorrect Simple Average} = \frac{10 + 0}{2} = \mathbf{5.0}$$

$$\text{Correct Total Weighted Average} = \frac{(2 \times 10) + (98 \times 0)}{100} = \mathbf{0.2}$$

---

## 2. Calculating Weighted Average Annual Price

To find the true average price per unit across a 12-month period:

$$\text{Weighted Annual Price} = \frac{\text{Total Revenue for the Year (\$)}}{\text{Total Units Sold for the Year (Qtd)}}$$

### Mathematical Proof

$$\text{Average Price} = \frac{\sum (\text{Price}_m \times \text{Volume}_m)}{\sum \text{Volume}_m} = \frac{\text{Total Annual Revenue}}{\text{Total Annual Units}}$$

By summing total dollars and dividing by total physical volume, each month is automatically weighted by its actual unit contribution.

---

## 3. Implementation in Code / Tools

### Excel
```excel
=SUM(C2:C13) / SUM(B2:B13)
```

### Power BI (DAX)
```dax
Weighted_Avg_Price = 
DIVIDE(
    SUM(Sales[Total_Revenue]), 
    SUM(Sales[Total_Units]), 
    0
)
```