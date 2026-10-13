# Minitab Statistical Analysis

## Project

**Improving Customer Order Fulfillment Reliability Using Lean Six Sigma DMAIC**

This folder contains the Minitab project files and exported outputs that are currently available for the project. The analyses support descriptive review and selected statistical checks of customer order fulfillment using a synthetic FMCG-style dataset.

> **Data disclosure:** The dataset is synthetic and intended for portfolio and learning purposes. Results do not represent actual performance at an employer or customer. Statistical association does not establish causation.

## Primary CTQ

**Customer Order Fulfillment**

The primary response measure is Customer Quantity Fill Rate:

\[
\text{Customer Quantity Fill Rate} = \frac{\text{Total Shipped Quantity}}{\text{Total Ordered Quantity}}\times 100
\]

The Minitab files use order-level and supplier-summary variables as described in each analysis below.

## Contents

```text
Minitab/
├── README.md
├── 01_Descriptive_Statistics/
│   ├── 01_Descriptive_Statistics.mpx
│   ├── 01_Descriptive_Statistics.pdf
│   ├── Distribution_of_Customer_Order_Quantity.pdf
│   ├── Distribution_of_Shipped_Quantity.pdf
│   └── Distribution_of_Shortage_Quantity.pdf
├── 02_Chi_Square_Category_Fulfillment/
│   ├── 02_Chi_Square_Category_Fulfillment.mpx
│   └── 02_Chi_Square_Category_Fulfillment.pdf
├── 03_Chi_Square_Warehouse/
│   ├── 03_Chi_Square_Warehouse_Fulfillment.mpx
│   └── 03_Chi_Square_Warehouse_Fulfillment.pdf
├── 04_Mann_Whitney_Test/
│   ├── 04_Mann_Whitney_Order_Quantity.mpx
│   └── 04_Mann_Whitney_Order_Quantity.pdf
└── 05_Correlation_Analysis/
    ├── 05_Spearman_Supplier_Fill_Rate.mpx
    ├── 05_Spearman_Supplier_Fill_Rate.pdf
    └── Matrix Plot of Supplier_PO_Fill_Rate, Customer_Quantity_Fill_Rate.png
```

## Analyses and available results

### 1. Descriptive statistics

**Files:** `01_Descriptive_Statistics/`

Includes a Minitab project and PDF outputs for descriptive statistics and distributions of:

- Customer order quantity (`Order_Qty`)
- Shipped quantity (`Shipped_Qty`)
- Shortage quantity (`Shortage_Qty`)

These outputs are used to review the scale and distribution of the quantity measures. This folder does not contain a dedicated Minitab Pareto analysis.

### 2. Category vs complete fulfillment — Chi-Square

**Files:** `02_Chi_Square_Category_Fulfillment/`

The cross-tabulation compares `Category` with `Complete_Flag` among eligible orders.

- Pearson Chi-Square: 2.650
- Degrees of freedom: 4
- P-value: 0.618

**Interpretation:** At \(\alpha=0.05\), this test does not identify a statistically significant association between category and complete-fulfillment status in this Minitab analysis.

### 3. Warehouse vs complete fulfillment — Chi-Square

**Files:** `03_Chi_Square_Warehouse/`

The cross-tabulation compares `Warehouse_ID` with `Complete_Flag` among eligible orders.

- Pearson Chi-Square: 4.208
- Degrees of freedom: 4
- P-value: 0.379
- Eligible orders shown in the output: 14,688

**Interpretation:** At \(\alpha=0.05\), this test does not identify a statistically significant association between warehouse and complete-fulfillment status.

The previously prepared Excel analysis recorded a different warehouse p-value (0.2902). Both results are non-significant, but the values are not an exact replication. The difference should remain documented until the input population, variable definitions, and analysis setup are reconciled.

### 4. Order quantity vs complete status — Mann–Whitney

**Files:** `04_Mann_Whitney_Test/`

The two-sample Mann–Whitney test compares `Order_Qty` for eligible incomplete and complete orders.

- Incomplete orders: \(n=1,793\); median order quantity = 148
- Complete orders: \(n=12,895\); median order quantity = 154
- Estimated median difference (incomplete minus complete): −2
- 95% confidence interval for the difference: (−6, 2)
- W-value: 13,015,059.50
- Tie-adjusted p-value: 0.361

**Interpretation:** At \(\alpha=0.05\), the test does not identify a statistically significant difference in order-quantity distributions between these groups. The result does not establish order quantity as a statistically validated driver based on this test alone.

### 5. Supplier PO fill rate vs customer quantity fill rate — Spearman correlation

**Files:** `05_Correlation_Analysis/`

The correlation uses 25 supplier-level rows, matching supplier PO fill-rate summaries with customer quantity fill-rate summaries for eligible sales orders.

- Spearman correlation: \(\rho=0.057\)
- Reported 95% confidence interval: (−0.346, 0.442)
- Rows used: 25

The Minitab output included in this folder does **not** display a p-value. The coefficient indicates a very weak positive rank association, and the reported confidence interval includes zero. Do not describe this as an exact replication of the earlier Excel result (\(\rho=0.009\), \(p=0.9651\)); the aggregation or definitions may differ. Any separately calculated p-value must be labelled as an external approximation, not a Minitab-reported value.

## Analyses not included in this Minitab folder

The current ZIP does not contain dedicated Minitab output folders for:

- Pareto analysis
- Logistic regression
- A consolidated statistical summary

Do not infer that these analyses were performed in Minitab based on this folder. Other project workbooks may contain related analysis, but those are separate artifacts.

## Interpretation and evidence limitations

- The results in this README describe the outputs currently present in this folder.
- Statistical significance is assessed at \(\alpha=0.05\) where a p-value is reported.
- Non-significant results do not prove that a relationship or effect is absent.
- The supplier correlation is based on only 25 aggregated supplier-level observations and is exploratory.
- The supplier correlation and warehouse Chi-Square results differ from previously documented Excel results; they should not be described as exact replications until the underlying definitions and calculations are reconciled.
- The available inventory snapshots do not necessarily represent inventory at the exact time each customer order was created, so these outputs alone cannot establish an inventory-related causal mechanism.

## Relationship to DMAIC

These files primarily support the **Measure** and **Analyze** phases by describing quantity distributions and testing selected associations or group differences. The outputs can inform further investigation, but they do not independently prove root causes or realized improvement.

## File guidance

- `.mpx` files are editable Minitab project files.
- `.pdf` files are exported analysis reports.
- The PNG file is the exported supplier correlation matrix plot.
- Backup `.bak` files have been removed from the portfolio folder and are therefore not listed in this contents section.