# 04. Assortment Breadth: Calculating SKUs per Store

To evaluate assortment depth and product line penetration across retail partners, we calculate the average number of SKUs stocked per store using **Numeric Distribution (ND)** figures.

---

## 1. The Formula

$$\text{Average SKUs Per Store} = \frac{\sum (\text{ND of Individual SKUs})}{\text{ND of Category / Brand Presence}}$$

---

## 2. Practical Calculation Matrix

Assume a market of **4 retail outlets** and a portfolio of **3 Toothpaste SKUs**:

| Outlet | SKU A | SKU B | SKU C | Total SKUs in Store |
| :--- | :---: | :---: | :---: | :---: |
| **Store 1** | Present | Present | Present | **3** |
| **Store 2** | Present | Present | Absent | **2** |
| **Store 3** | Present | Absent | Absent | **1** |
| **Store 4** | Absent | Absent | Absent | **0** |
| **SKU ND (%)** | **75%** (3/4) | **50%** (2/4) | **25%** (1/4) | — |

### Computation

$$\sum \text{NDs} = 75\% + 50\% + 25\% = 150\%$$

1. **Across All Market Stores (Category ND = 100%):**
   $$\text{Avg. SKUs / All Stores} = \frac{150\%}{100\%} = \mathbf{1.5 \text{ SKUs / store}}$$

2. **Across Active Brand Stores Only (Brand ND = 75%):**
   $$\text{Avg. SKUs / Active Stores} = \frac{150\%}{75\%} = \mathbf{2.0 \text{ SKUs / active store}}$$