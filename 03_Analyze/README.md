# 03 — Analyze

## Purpose

The Analyze phase investigates sources of variation in customer order fulfillment and distinguishes factors supported by the available data from factors that were not supported as primary discriminators.

## Analytical Questions

The analysis focuses on:

1. Where is fulfillment variation concentrated?
2. Which product/category patterns are associated with fulfillment performance?
3. Does order quantity differ between complete and incomplete fulfillment?
4. Does warehouse appear to be a primary discriminator?
5. Does supplier performance appear to explain customer fulfillment variation?
6. What limitations prevent stronger causal conclusions?

## Key Findings

### Statistically Tested Factors

The completed statistical tests did not identify order quantity or product category as statistically significant factors at the 0.05 significance level.

- **Product category:** The chi-square test did not identify a statistically significant association with complete-fulfillment status (p = 0.6179).
- **Order quantity:** The Mann–Whitney test did not identify a statistically significant difference in order-quantity distributions between eligible complete and incomplete orders (p = 0.3611).
- **Warehouse:** The Minitab chi-square test did not identify a statistically significant association with complete-fulfillment status (p = 0.3786).
- **Supplier performance:** The supplier-level Spearman correlation was very weak (ρ = 0.057), with a reported 95% confidence interval of (−0.346, 0.442). The available Minitab output does not report a p-value.

These results do not prove that the factors have no relationship with fulfillment. They indicate that the completed tests did not establish statistically significant associations or differences.

### Descriptive Findings and Improvement Opportunities

- The largest order-size band contributed the highest absolute shortage quantity (59,261 units), but its fill rate was approximately 92.57%, higher than the rates for the two smallest bands.
- Category-level fill rates and complete-order rates vary descriptively, but the category chi-square test did not establish a statistically significant association.
- Order-size exception review and category-level monitoring may be evaluated as pilot interventions. Neither should be presented as a response to a statistically proven root cause.

### Factors Requiring Further Investigation

The available analysis does not establish warehouse or supplier purchase-order fill performance as statistically significant discriminators of complete fulfillment.

Supplier correlation results should remain exploratory because they use only 25 supplier-level observations. The supplier and warehouse results also differ from earlier Excel outputs, so their calculation setups should be reconciled before claiming exact replication.

## Advanced Analysis

The advanced analysis includes:

- Category analysis
- Order quantity bands
- Logistic regression
- Root-cause evidence assessment
- Fishbone candidates
- 5 Why validation

The logistic model is treated as descriptive/in-sample analytical evidence rather than as a validated predictive model.

## Analyze-Phase Artifacts

| File | Description |
|---|---|
| `03_Analyze_LSSBB_Artifacts.xlsx` | Core Analyze-phase workbook |
| `03_Analyze_LSSBB_Advanced_Artifacts.xlsx` | Advanced statistical and root-cause analysis |
| `order_fulfillment_analytical_dataset.csv` | Analytical dataset prepared for the Analyze phase |

## Evidence Boundary

The findings indicate association with fulfillment performance; they do not establish causality.

Important operational variables were unavailable, including:

- Inventory position at the exact time of order
- Allocation timestamps
- Picking/workload information
- Standardized shortage reason codes

The dataset is synthetic and should not be presented as actual employer performance.