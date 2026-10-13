# 02 — Measure

## Purpose

The Measure phase establishes operational definitions, validates the available data, defines the measurement system, and establishes the baseline performance of the customer order fulfillment process.

## Measurement Focus

The primary measurement is:

**Customer Quantity Fill Rate**

> Total Shipped Quantity ÷ Total Ordered Quantity × 100

Both all-order and non-cancelled/eligible views are retained to make the treatment of cancelled orders transparent.

## Key Measures

The Measure phase defines and evaluates:

- Customer Quantity Fill Rate
- Complete Order Fulfillment Rate
- Partial Fulfillment Rate
- Backorder Rate
- Cancellation Rate
- Shortage Quantity
- On-Time Delivery Rate
- Supplier Fill Rate

## Baseline

The documented baseline includes:

- Approximately 15,000 sales orders
- Overall customer quantity fill rate: **90.30%**
- Non-cancelled customer quantity fill rate: **92.21%**
- Complete order fulfillment rate: **87.79%** for the non-cancelled/eligible view
- Backorder rate: **5.27%**
- Partial fulfillment rate: **6.94%**
- Eligible shortage quantity: **174,549 units**
- Supplier fill rate: approximately **86.32%**

## Data Quality

The data-quality audit evaluates:

- Record counts
- Duplicate records
- Missing values
- Quantity validity
- Date validity
- Ordered versus shipped quantity consistency
- Status consistency

No duplicate sales orders were identified, and no negative ordered or shipped quantities were identified.

## Measurement Lesson

The difference between the all-order fill rate and non-cancelled fill rate is a measurement-definition issue rather than a data-quality error.

Cancelled orders are therefore retained as a separate outcome rather than being mixed with backorders or partial fulfillment.

## Measure-Phase Artifacts

| File | Description |
|---|---|
| `02_Measure_LSSBB_Artifacts.xlsx` | Consolidated Measure-phase workbook containing the Measurement Plan, Data Dictionary, Data Quality Audit, Baseline Analysis, and Order Status Profile |

## Evidence Boundary

The baseline represents the available synthetic dataset. It should not be interpreted as actual company or employer performance.