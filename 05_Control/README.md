# 05 — Control

## Purpose

The Control phase converts the DMAIC findings into a proposed monitoring system, control plan, reaction plan, and standardization framework.

## Core Control KPIs

The control framework monitors:

- Customer Quantity Fill Rate
- Complete Order Fulfillment Rate
- Backorder Rate
- Partial Fulfillment Rate
- Shortage Quantity
- Shortage Reason Code Completeness
- Inventory Snapshot Completeness

## Monitoring Approach

The proposed monitoring approach uses weekly fulfillment KPI trends and exception monitoring. The weekly trend in this portfolio is based on a synthetic baseline dataset; it is not evidence of post-improvement performance or validated production process stability.

The Power BI dashboard provides the proposed operational monitoring interface. Before operational use, validate KPI definitions, data completeness, reporting cadence, and escalation thresholds against actual production data.

## Reaction Plan

### Fill-Rate Deterioration

Review:

- Affected order-size bands
- Product/category performance
- Recent shortage patterns

### Backorder Increase

Review:

- Inventory availability
- Replenishment status
- Affected products/categories

### Partial Fulfillment Increase

Review:

- Allocation behavior
- Fulfillment exceptions
- Order-size patterns

### Missing Shortage Reasons

Investigate:

- Data-capture compliance
- Exception coding
- Standardization adherence

### Missing Inventory Snapshots

Investigate:

- Inventory data completeness
- Snapshot generation
- Data availability before using the metric for operational decisions

## SPC Guidance

The project recommends using appropriate monitoring methods such as weekly p-charts or run charts where sufficient production data is available.

Validated production control limits are **not claimed from the synthetic baseline**.

## Power BI Dashboard

The Power BI control dashboard contains:

- Executive KPI monitoring
- Diagnostic analysis
- Weekly fulfillment trend
- Reaction-plan guidance
- Control strategy

## Control Strategy

> **Monitor → Review → Investigate → React → Standardize**

## Control-Phase Artifacts

| File | Description |
|---|---|
| `05_Control_LSSBB_Artifacts.xlsx` | Consolidated Control-phase workbook containing the Control Plan, KPI Definitions, SPC Guidance, Reaction Plan, Dashboard Specification, Standardization Handoff, DMAIC Linkage, and Baseline Trend |

## Evidence Boundary

This Control phase describes a proposed control system.

The project does not claim:

- Demonstrated statistical process stability
- Realized post-improvement performance
- Actual operational deployment
- Actual employer performance improvement

The dataset is synthetic and is used for portfolio demonstration.