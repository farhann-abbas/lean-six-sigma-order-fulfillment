# Data

## Purpose

This folder contains the synthetic FMCG-style supply chain datasets used for the Lean Six Sigma Black Belt DMAIC project.

The data is used to demonstrate supply chain analytics, Lean Six Sigma measurement, statistical analysis, improvement planning, and control design.

## Dataset Disclaimer

**The datasets are synthetic and are not confidential company data.**

They are intended for portfolio, educational, analytical, and methodology-demonstration purposes.

Results from this dataset should not be interpreted as actual employer or customer performance.

## Source Tables

The project contains seven primary source datasets.

| Dataset | Purpose |
|---|---|
| `products.csv` | Product/SKU master data including supplier, lead time, safety stock, reorder point, and shelf life |
| `suppliers.csv` | Supplier master data and supplier characteristics |
| `warehouses.csv` | Distribution-center/warehouse master data |
| `customers.csv` | Customer master data and customer type information |
| `inventory.csv` | Daily product/warehouse inventory movement and closing-stock information |
| `sales_orders.csv` | Customer sales-order transactions including ordered and shipped quantities |
| `purchase_orders.csv` | Supplier purchase-order transactions including ordered and received quantities |

## Approximate Dataset Scale

The project dataset contains approximately:

- 150 products
- 25 suppliers
- 5 warehouses
- 80 customers
- 15,000 sales orders
- 5,000 purchase orders
- 16,000+ inventory records

## Key Relationships

The datasets can be conceptually connected through:

- Product
- Supplier
- Warehouse
- Customer
- Sales Order
- Purchase Order
- Inventory date/product/warehouse relationships

The detailed data dictionary and analytical relationships are documented in the Measure and Analyze phase workbooks.

## Data Preparation

The project workflow uses:

> Raw CSV Data → Initial Review → PostgreSQL/SQL → Analytical Dataset → Statistical Analysis → Power BI

The analytical dataset used for the Analyze phase is located in:

```text
03_Analyze/order_fulfillment_analytical_dataset.csv
```

## Data Quality and Limitations

The analytical dataset has known data-quality limitations that should be considered when interpreting results.

- **Missing delivery dates:** 1,085 sales-order records have missing delivery dates. On-time delivery metrics calculated only from records with available dates may not represent overall order performance.
- **Missing purchase-order receipt dates:** 417 purchase-order records have missing actual receipt dates. Supplier lead-time and delivery-performance analysis may therefore be incomplete.
- **Inventory snapshot matching:** The available inventory records do not provide a reliable prior-day inventory match for every sales order. Inventory-at-order conclusions should be treated as exploratory.
- **Synthetic data:** Relationships and patterns in this dataset are intended to demonstrate analytical methods and are not evidence of actual business performance or causal mechanisms.

Before operational use, reconcile missing dates, validate source-system definitions, document exclusions, and confirm KPI calculations against production records.

## Interpretation of Analytical Results

Descriptive differences between products, categories, warehouses, suppliers, and order-size bands should not automatically be interpreted as statistically significant relationships or proven root causes. Hypotheses and improvement actions should be validated using appropriate statistical tests and, where applicable, operational pilot results.