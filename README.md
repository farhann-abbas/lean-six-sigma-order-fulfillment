# Lean Six Sigma Black Belt — Customer Order Fulfillment Reliability

## Project Overview

**Project:** Improving Customer Order Fulfillment Reliability Using Lean Six Sigma DMAIC

This portfolio project applies the **Lean Six Sigma DMAIC methodology** to customer order fulfillment using a synthetic FMCG-style supply-chain dataset.

The project complements my existing **Supply Chain Analytics** portfolio project:

- **Supply Chain Analytics:** What is happening in the supply chain?
- **Lean Six Sigma DMAIC:** Why is fulfillment performance varying, what factors are associated with the variation, and how can the process be improved and controlled?

---

## Business Problem

Customer orders are not consistently fulfilled in full. The project establishes a measurable baseline, separates different fulfillment outcomes, investigates sources of variation, identifies factors supported by the available data, proposes process improvements, and establishes a control framework.

The project does **not** claim that a specific root cause has been proven causal unless the available data supports that conclusion.

---

## Primary CTQ and Y

### Primary CTQ
**Customer Order Fulfillment**

### Primary Y
**Customer Quantity Fill Rate**

Initial operational definition:

> Total Shipped Quantity / Total Ordered Quantity × 100

Two reporting views are retained during measurement:

- **All-order quantity fill rate:** approximately **90.30%**
- **Non-cancelled quantity fill rate:** approximately **92.21%**

Cancellation is retained as a separate outcome rather than silently treating it as the same phenomenon as partial fulfillment or backorders.

---

# DMAIC Approach

## 1. Define

Key artifacts:

- Project Charter
- SIPOC
- Voice of Customer / CTQ framework
- Stakeholder framing
- Current-state process boundary

The available dataset does not contain customer interviews, surveys, complaint transcripts, or direct VOC records. Therefore, customer requirements are translated into measurable CTQs without claiming that interviews were conducted.

### Process boundary

Customer Order Created → Order Processing → Inventory Availability Check → Allocation → Replenishment if Required → Picking/Fulfillment → Shipment → Customer Order Fulfilled/Unfulfilled

---

## 2. Measure

The Measure phase establishes the measurement system and baseline.

### Data

The project uses a synthetic FMCG-style dataset containing:

- Products
- Suppliers
- Warehouses
- Customers
- Inventory
- Sales Orders
- Purchase Orders

The dataset contains approximately:

- 15,000 sales orders
- 5,000 purchase orders
- 150 products
- 25 suppliers
- 5 warehouses
- 80 customers

### Baseline observations

| Measure | Baseline |
|---|---:|
| Sales orders | ~15,000 |
| All-order quantity fill rate | ~90.30% |
| Non-cancelled quantity fill rate | ~92.21% |
| Cancellation rate | ~2.08% |
| Supplier fill rate | ~86.32% |

The Measure phase also performs data-quality checks for duplicates, missing values, invalid quantities, date inconsistencies, and other structural issues.

---

## 3. Analyze

The Analyze phase separates **observed evidence, hypotheses, statistical evidence, and operational interpretation**.

### Statistical findings

The completed statistical tests did not establish order quantity or product category as statistically significant factors at the 0.05 significance level.

- **Product category:** The chi-square test did not identify a statistically significant association with complete-fulfillment status (p = 0.6179).
- **Order quantity:** The Mann–Whitney test did not identify a statistically significant difference in order-quantity distributions between eligible complete and incomplete orders (p = 0.3611).
- **Warehouse:** The Minitab chi-square test did not identify a statistically significant association with complete-fulfillment status (p = 0.3786).
- **Supplier performance:** The supplier-level Spearman correlation was very weak (ρ = 0.057), with a reported 95% confidence interval of (−0.346, 0.442). The available Minitab output does not report a p-value.

Non-significant results do not prove that relationships are absent. The findings indicate that the completed tests did not establish statistically significant associations or differences.

### Descriptive findings and improvement opportunities

- The largest order-size band contributed the highest absolute shortage quantity (59,261 units), but its fill rate was approximately 92.57%, higher than the rates for the two smallest bands.
- Category-level performance varies descriptively, but the category chi-square test did not establish a statistically significant association.
- Order-size exception review and category-level monitoring may be evaluated as pilot interventions. Neither should be presented as a response to a statistically proven root cause.

### Important data limitation

The dataset does not provide sufficient operational detail to establish a causal inventory mechanism at the order-event level. In particular, it lacks items such as:

- inventory-at-order-time snapshots
- allocation timestamps
- picking capacity/workload
- standardized shortage/exception reason codes

Therefore, inventory-related mechanisms remain an important **data gap / hypothesis**, not a proven root cause.

### Advanced analysis

The project includes:

- Pareto analysis
- Category analysis
- Order-quantity segmentation
- Correlation analysis
- Hypothesis testing
- Logistic regression as descriptive/in-sample analysis
- Fishbone candidates
- 5 Whys validation framework

The logistic model is explicitly treated as **descriptive/in-sample evidence**, not as a validated production prediction model.

---

## 4. Improve

The Improve phase converts the supported findings into process-oriented improvement proposals.

### Proposed improvements

The following actions are proposed pilot interventions and data-quality improvements. They are not solutions to statistically proven root causes.

1. **Order-size risk flag:** Pilot enhanced inventory and allocation review for selected high-quantity orders; validate the outcome before scaling.
2. **Category-level monitoring:** Track category-level patterns without treating category as a proven cause or introducing unsupported category-specific rules.
3. **Exception-based allocation review:** Pilot a defined exception pathway and evaluate its effectiveness against a baseline.
4. **Inventory-at-order measurement:** Capture inventory position when each customer order is created to support future root-cause analysis.
5. **Standardized shortage reason codes:** Improve the consistency and completeness of shortage and incomplete-fulfillment records.

### FMEA

The FMEA prioritizes risks such as:

- Large customer order not being fully fulfilled
- Category-specific shortages not being proactively identified
- Allocation without reliable inventory-at-order visibility
- Missing shortage reason information

Supplier performance is retained as a contextual factor rather than targeted as a primary improvement cause.

### Scenario analysis

Projected scenarios model 5%, 10%, and 15% shortage reduction.

These are explicitly **assumptions/scenarios**, not realized improvements.

---

## 5. Control

The Control phase establishes how the improved process should be monitored.

### Core control KPIs

- Customer Quantity Fill Rate
- Complete Order Fulfillment Rate
- Backorder Rate
- Partial Fulfillment Rate
- Shortage Quantity
- Shortage Reason Code Completeness
- Inventory Snapshot Completeness

### Control strategy

The control framework includes:

- weekly KPI monitoring
- segment-level Pareto analysis
- order-size and category monitoring
- exception review
- standardized shortage coding
- inventory snapshot completeness
- defined reaction plans

SPC guidance is included, with the explicit rule that **synthetic-baseline limits must not be presented as production control limits**.

---

# Key Portfolio Takeaway

This project demonstrates the difference between **analytics and process improvement**.

### Analytics project

> Describes supply-chain performance using SQL, Excel, Python and Power BI.

### Lean Six Sigma project

> Uses DMAIC to define a CTQ, establish a measurement system, investigate variation statistically, distinguish supported factors from hypotheses, design improvements, and establish controls.

This creates a complementary portfolio narrative rather than two projects doing the same job.

---

# Tools

- **Minitab** — Lean Six Sigma statistical analysis
- **Excel** — DMAIC artifacts, FMEA, measurement and control plans
- **PostgreSQL / SQL** — data preparation and analytical dataset creation
- **DBeaver** — database analysis
- **Python** — validation, EDA and reproducibility
- **Power BI** — LSSBB control dashboard
- **draw.io / diagrams.net** — process maps and visual analysis
- **PowerPoint** — final case-study presentation
- **Git / GitHub** — version control and portfolio presentation

---

## Power BI LSSBB Control Dashboard

The Power BI dashboard translates the DMAIC analysis into an operational monitoring and control view.

### Dashboard Pages

#### 01 — Control Dashboard
Provides the overall fulfillment baseline and KPI monitoring view.

Key metrics:
- Customer Quantity Fill Rate: 90.3%
- Complete Order Fulfillment Rate: 87.8%
- Backorder Rate: 5.2%
- Partial Fulfillment Rate: 6.8%
- Eligible Shortage Quantity: 174,549 units

Key visuals:
- Weekly customer quantity fill rate
- Fill rate by product category
- Fill rate by order quantity band

#### 02 — Diagnostic Analysis
Focuses on identifying where fulfillment variation and shortage concentration occur.

Key findings:
- The largest order-size band contributed the highest absolute shortage quantity, but the order-quantity hypothesis test was not statistically significant.
- Product category showed descriptive variation, but the chi-square test did not establish a statistically significant association with complete-fulfillment status.
- Warehouse was not supported as a statistically significant discriminator in the Minitab chi-square test.
- Supplier PO fill performance showed a very weak supplier-level rank correlation with customer fill; the available Minitab output does not report a p-value.
- Findings are exploratory and descriptive; causality is not established by the available synthetic dataset.

#### 03 — Control & Reaction
Translates the analysis into a proposed operational control framework.

Control approach:
- Monitor weekly fulfillment KPIs
- Review exception trends and deterioration
- Investigate order-size/category patterns and inventory availability
- React using defined exception-response actions
- Standardize KPI definitions, shortage coding, and inventory snapshot completeness

The dashboard uses a monitoring trend rather than claiming demonstrated SPC control limits because the available dataset is synthetic and does not contain a post-improvement production period.

### Dashboard Architecture

```text
DMAIC Analysis
      ↓
Documented KPI Definitions
      ↓
Power BI Control Dashboard
      ↓
Diagnostic Analysis
      ↓
Reaction Plan
      ↓
Control & Standardization
```

# Repository Structure

```text
lean-six-sigma-order-fulfillment/
│
├── 01_Define/
│   ├── 01_Define_LSSBB_Artifacts.xlsx
│   └── README.md
│
├── 02_Measure/
│   ├── 02_Measure_LSSBB_Artifacts.xlsx
│   └── README.md
│
├── 03_Analyze/
│   ├── 03_Analyze_LSSBB_Artifacts.xlsx
│   ├── 03_Analyze_LSSBB_Advanced_Artifacts.xlsx
│   ├── order_fulfillment_analytical_dataset.csv
│   ├── README.md
│   └── Minitab/
│       ├── 01_Descriptive_Statistics/
│       ├── 02_Chi_Square_Category_Fulfillment/
│       ├── 03_Chi_Square_Warehouse/
│       ├── 04_Mann_Whitney_Test/
│       └── 05_Correlation_Analysis/
│
├── 04_Improve/
│   ├── 04_Improve_LSSBB_Artifacts.xlsx
│   └── README.md
│
├── 05_Control/
│   ├── 05_Control_LSSBB_Artifacts.xlsx
│   └── README.md
│
├── 06_Power_BI/
│   ├── LSSBB_Order_Fulfillment_Control.pbix
│   ├── README.md
│   └── [three dashboard screenshots are stored in screenshots/]
│
├── data/
│   ├── customers.csv
│   ├── inventory.csv
│   ├── products.csv
│   ├── purchase_orders.csv
│   ├── sales_orders.csv
│   ├── suppliers.csv
│   ├── warehouses.csv
│   └── README.md
│
├── presentation/
│   └── LSSBB_Order_Fulfillment_Black_Belt_Case_Study.pptx
│
├── screenshots/
│   ├── 01_Control_Dashboard.png
│   ├── 02_Diagnostic_Analysis.png
│   └── 03_Control_&_Reaction.png
│
├── PORTFOLIO_CHECKLIST.md
└── README.md
```

---

## Data Quality Limitations

The synthetic dataset has known limitations that affect interpretation:

- **Missing delivery dates:** 1,085 sales-order records have missing delivery dates, limiting on-time delivery analysis.
- **Missing purchase-order receipt dates:** 417 purchase-order records have missing actual receipt dates, limiting supplier delivery-performance analysis.
- **Inventory matching:** Prior-day inventory records do not reliably match every sales order. Inventory-at-order mechanisms remain exploratory.
- **No post-improvement production period:** Scenario impacts and weekly baseline trends do not demonstrate realized improvements or production process stability.

These limitations should be resolved or explicitly accounted for before using the findings for operational decisions.

# Data & Ethics

This project uses **synthetic data** designed for portfolio and analytical demonstration.

It must not be presented as confidential employer data or as measured operational performance from Pride Of India FMCG or another real organization.

No employer-specific improvement claim is made.

---

# LSSBB Methodology

The project follows the DMAIC logic:

**Define → Measure → Analyze → Improve → Control**

The central methodological rule is:

> Do not declare a root cause or improvement result before the available evidence supports it.

Where the dataset is insufficient, the project identifies the limitation and proposes the additional measurement needed for future validation.

---

## Portfolio Status

- [x] Define
- [x] Measure
- [x] Analyze
- [x] Improve
- [x] Control
- [ ] Final Power BI control dashboard
- [ ] Final case-study presentation
- [ ] GitHub screenshots / visual polish
