# 04 — Improve

## Purpose

The Improve phase converts the evidence from the Analyze phase into prioritized improvement opportunities and a future-state fulfillment process.

## Improvement Principle

Improvement actions were selected based on the documented evidence and FMEA prioritization.

The project does not claim realized improvement because no post-improvement production dataset is available.

## Prioritized Improvement Actions

The following actions are proposed pilot interventions and data-quality improvements based on descriptive findings, operational considerations, and FMEA review. They are not confirmed solutions to statistically validated root causes.

### 1. Order-Size Risk Flag

Pilot an enhanced inventory availability and allocation review for selected high-quantity orders. The largest order-size band has the highest absolute shortage quantity, but its fill rate is approximately 92.57%, and the Mann–Whitney test did not identify a statistically significant difference in order-quantity distributions between eligible complete and incomplete orders (p = 0.3611). Validate the pilot using defined outcome measures before wider rollout.

### 2. Category-Level Monitoring

Monitor category-level fulfillment and shortage patterns to identify changes that may warrant investigation. The chi-square test did not identify a statistically significant association between product category and complete-fulfillment status (p = 0.6179). Do not treat category as a proven root cause or introduce category-specific rules without further operational evidence.

### 3. Inventory-at-Order Measurement

Capture inventory position at the time each customer order is created. This data-quality improvement is intended to support stronger future root-cause analysis; the current project does not establish inventory availability at order creation as a proven cause of incomplete fulfillment.

### 4. Standardized Shortage Reason Codes

Capture standardized, consistently defined reasons for shortages and incomplete fulfillment. Review completeness and accuracy of the recorded reasons before using them to make causal conclusions.

### 5. Exception-Based Allocation Review

Pilot an exception pathway for orders that require additional allocation or fulfillment review. Define the eligibility criteria, responsible roles, and outcome measures in advance, then evaluate the pilot against an appropriate baseline before deciding whether to scale it.

## FMEA Prioritization

The FMEA identifies proposed process risks for further evaluation. Detection ratings are provisional assumptions, and the resulting RPN values are prioritization aids rather than proof of root causes.

| Failure Mode | RPN |
|---|---:|
| Large customer order not fully fulfilled | 256 |
| Category-specific shortage not proactively identified | 224 |
| Allocation without reliable inventory-at-order snapshot | 216 |
| Shortage reason not captured | 168 |
| Supplier performance incorrectly targeted | 84 |

## Future-State Process

The proposed future-state process is:

> Order Created → Risk Screening → Inventory Check → Allocation → Replenishment Check → Fulfillment → Exception Capture → Control Feedback

## Scenario Analysis

Scenario impacts in the Improve workbook are **projected assumptions**, not realized improvements.

They are used to illustrate the potential effect of shortage reduction scenarios.

## Improve-Phase Artifacts

| File | Description |
|---|---|
| `04_Improve_LSSBB_Artifacts.xlsx` | Consolidated Improve-phase workbook containing FMEA, improvement actions, prioritization, scenario impact, future-state process, and control handoff |

## Evidence Boundary

The improvement actions represent proposed process improvements based on the available evidence. They were not implemented in a live operational environment as part of this portfolio project.