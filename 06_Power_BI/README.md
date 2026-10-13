# 06 — Power BI

## Purpose

This folder contains the Power BI dashboard developed to translate the Lean Six Sigma DMAIC analysis into an operational monitoring and control interface.

## Power BI File

| File | Description |
|---|---|
| `LSSBB_Order_Fulfillment_Control.pbix` | Power BI dashboard containing the Control, Diagnostic Analysis, and Control & Reaction pages |

## Dashboard Pages

### 01 — Control Dashboard

Provides the overall fulfillment baseline and KPI monitoring view.

Key metrics include:

- Customer Quantity Fill Rate
- Complete Order Fulfillment Rate
- Backorder Rate
- Partial Fulfillment Rate
- Eligible Shortage Quantity

### 02 — Diagnostic Analysis

Shows:

- Order status distribution
- Shortage by product category
- Fill rate by order quantity band
- Overall versus non-cancelled fulfillment performance
- Shortage quantity by order quantity band
- Supported versus unsupported analytical factors
- Improvement focus

### 03 — Control & Reaction

Shows:

- Fulfillment KPI monitoring
- Weekly non-cancelled fulfillment trend
- Control KPI summary
- Reaction plan
- Control strategy

## Dashboard Logic

The dashboard uses KPI definitions documented during the Measure and Control phases. These definitions support consistent portfolio analysis, but their data completeness, calculation logic, and operational applicability should be validated against actual production data before deployment.

Diagnostic charts show descriptive patterns, not proof of root causes. The category-versus-complete-fulfillment test was not statistically significant (p = 0.6179), and the order-quantity comparison was not statistically significant (p = 0.3611). The largest order-size band has the highest absolute shortage quantity (59,261), but its fill rate is approximately 92.57%; this should not be interpreted as evidence of disproportionately high shortage risk.

The dashboard distinguishes:

- All-order performance
- Non-cancelled/eligible performance
- Complete fulfillment
- Backorders
- Partial fulfillment
- Shortage quantity

## Control Approach

The dashboard supports the proposed control strategy:

> Monitor → Review → Investigate → React → Standardize

## Evidence Boundary

The dashboard is based on a synthetic dataset.

It represents a proposed LSSBB monitoring and control framework and does not claim actual production deployment, statistical process stability, or realized improvement.