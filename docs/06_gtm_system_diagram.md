# 06. FMCG Distribution System Diagram

This page contains the architecture diagram for Go-To-Market distribution analytics, ready for rendering natively in Markdown tools, GitHub, or importing into **Excalidraw**.

---

## 1. Mermaid System Architecture

```mermaid
flowchart TD
    subgraph Core_Metrics["1. Core Metrics (ND vs. WD)"]
        ND["Numeric Distribution (ND)<br/><b>Stores with Product / Total Stores</b><br/><i>(Measures Physical Reach)</i>"]
        WD["Weighted Distribution (WD / DP)<br/><b>Category Sales in Stores with Product / Total Category Sales</b><br/><i>(Measures Market Potential)</i>"]
    end

    subgraph Combined_Metrics["2. Derived Metrics & Key Formulas"]
        SKU_Store["Avg. SKUs Per Store<br/><b>Sum of Individual NDs ÷ Total Category ND</b><br/><i>(Assortment Breadth / Depth)</i>"]
        Eff_Ratio["Efficiency Ratio<br/><b>WD ÷ ND</b><br/><i>(Quality Ratio: > 1.0 = High Volume Stores)</i>"]
        FS_Gap["Fair Share Gap<br/><b>WD - ND</b><br/><i>(Growth Opportunity Gap)</i>"]
        Price_Avg["Weighted Avg. Annual Price<br/><b>Total Revenue ÷ Total Units Sold</b><br/><i>(Avoids Average of Averages)</i>"]
    end

    subgraph Scenarios["3. Strategic Matrix (ND vs. WD)"]
        HighWD_LowND["High WD (80%) / Low ND (40%)<br/><b>High Efficiency</b><br/>Present in top Key Accounts"]
        HighND_LowWD["High ND (80%) / Low WD (40%)<br/><b>High Dispersion</b><br/>Present in many small, low-volume stores"]
        HighBoth["High ND (95%) & High WD (95%)<br/><b>Total Market Reach</b><br/>Maximum distribution achieved"]
    end

    subgraph Diagnosis["4. Low Market Share Diagnosis (High WD/ND 95%)"]
        Exec["Execution Issues<br/>• Ghost Inventory / OOS<br/>• Poor Shelf Placement (Bottom Shelf)"]
        ValueProp["Price & Value<br/>• High Price Index vs. Competitors<br/>• Low Pull / Weak Marketing Support"]
        Niche["Portfolio Role<br/>• Niche / Specialty SKU"]
    end

    ND --> Eff_Ratio
    WD --> Eff_Ratio
    ND --> FS_Gap
    WD --> FS_Gap
    ND --> SKU_Store
    
    WD --> HighWD_LowND
    ND --> HighND_LowWD
    WD & ND --> HighBoth

    HighBoth -->|"If Market Share remains low"| Diagnosis
    Diagnosis --> Exec
    Diagnosis --> ValueProp
    Diagnosis --> Niche
```

---

## 2. How to Import to Excalidraw

1. Copy the raw Mermaid code block above.
2. Open [Excalidraw](https://excalidraw.com/).
3. Open **More Tools** (`+` icon on top bar) $\rightarrow$ **Mermaid to Excalidraw**.
4. Paste the code and click **Insert**.