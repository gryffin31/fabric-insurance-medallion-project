# Insurance Analytics Using Microsoft Fabric

An end-to-end insurance analytics project built using Microsoft Fabric and PySpark, following the Medallion Architecture (Bronze, Silver, and Gold).

## Project Overview

This project processes customer, policy, and claims data through a Lakehouse-based data engineering workflow. The cleaned and aggregated data supports insurance analysis and Power BI reporting.

## Technology Stack

- Microsoft Fabric
- Fabric Lakehouse
- PySpark
- Delta Lake
- Direct Lake semantic model
- Power BI
- GitHub

## Architecture

- **Bronze:** Raw customer, policy, and claims CSV files.
- **Silver:** Cleaned and transformed Delta tables.
- **Gold:** Aggregated customer-level insurance analytics.

## Datasets

- `customers.csv` — Customer details
- `policies.csv` — Insurance policy information
- `claims.csv` — Insurance claims information

## Key Analysis

- Total claims and claim amounts by customer
- Approved and rejected claims
- Approval rate by gender
- Claim-to-coverage ratio
- Customers by policy type
- High-value customers by claim amount

## Gold Table

The aggregated output is stored in the `insurance_aggrgate` table and used as the source for the Direct Lake semantic model.

## Workflow

1. Load raw CSV files into the Fabric Lakehouse.
2. Clean and transform the data using PySpark.
3. Save the transformed data as Silver Delta tables.
4. Join and aggregate data to create Gold-level analytics.
5. Create a semantic model in Microsoft Fabric.
6. Build a Power BI report using the Gold data.

## Project Structure

```text
fabric-insurance-medallion-project/
├── data/
│   ├── customers.csv
│   ├── policies.csv
│   └── claims.csv
├── notebooks/
│   └── Insurance_Medallion_Notebook.ipynb
├── images/
└── README.md
```

## Note

This project was developed in Microsoft Fabric. Dataset files, notebook outputs, and screenshots can be added to this repository to document the workflow and results.
