# Procurement Analytics using Databricks & Power BI

## Project Overview

This project demonstrates an end-to-end Procurement Analytics solution built using **Databricks**, **PySpark**, **Delta Lake**, and **Power BI** following the **Medallion Architecture (Bronze → Silver → Gold)**.

The objective is to simulate an enterprise-grade data engineering and business intelligence solution for the Procure-to-Pay (P2P) business process.

The project focuses on industry-standard coding practices, reusable ETL components, data quality, audit logging, and interactive Power BI dashboards.

---

# Business Objective

The Procurement department requires a centralized reporting solution to monitor and analyze the complete Procure-to-Pay lifecycle.

This solution enables business users to:

- Monitor Purchase Requisitions
- Track Purchase Orders
- Analyze Goods Receipts
- Monitor Invoice Processing
- Track Supplier Payments
- Measure Procurement KPIs
- Improve Data Quality
- Detect Duplicate Transactions
- Improve Supplier Performance

---

# Project Architecture

```
                CSV Files
                     │
                     ▼
                Catalog (Volume)
                     |
                     ▼
             Bronze Layer
          (Raw Delta Tables)
                     │
                     ▼
             Silver Layer
     (Cleaned & Validated Data)
                     │
                     ▼
              Gold Layer
      (Star Schema Model)
                     │
                     ▼
            Power BI Desktop
                     │
                     ▼
          Procurement Dashboard
```
<img width="1912" height="673" alt="image" src="https://github.com/user-attachments/assets/00038db9-e959-4b31-a4ea-884731d20e86" />

---

# Technology Stack

| Technology | Purpose |
|------------|---------|
| Databricks Free Edition | Data Engineering |
| PySpark | Data Processing |
| Delta Lake | Storage Format |
| Unity Catalog | Metadata Management |
| Power BI Desktop | Reporting |
| GitHub | Version Control |
| SQL | Data Validation |

---

# Project Folder Structure

```
Procurement-Analytics/

│
├── notebooks/
│
│   ├── 01_Config
│   ├── 02_Bronze
│   ├── 03_Silver
│   ├── 04_Gold
│   ├── 05_Helper_Functions
│   ├── 06_SQL
│   └── 07_Testing
│
├── powerbi/
│
├── sql/
│
├── architecture/
│
├── images/
│
├── datasets/
│
└── README.md
```

---
<img width="1917" height="555" alt="image" src="https://github.com/user-attachments/assets/0ff211ee-ba86-4304-845f-3817e6a19f93" />

# Medallion Architecture

## Bronze Layer

Purpose

- Load raw CSV files
- Preserve original data
- Add audit columns
- Capture duplicate records

Tables

- bronze_departments
- bronze_employees
- bronze_suppliers
- bronze_products
- bronze_purchase_requisitions
- bronze_purchase_orders
- bronze_goods_receipts
- bronze_invoices
- bronze_payments
  
<img width="1918" height="386" alt="image" src="https://github.com/user-attachments/assets/752f17c9-ff88-4f2c-8c4c-da53cd8ab9ba" />

---

## Silver Layer

Purpose

- Data Cleaning
- Duplicate Removal
- Null Handling
- Data Type Validation
- Business Rule Validation
- Standardization

---

## Gold Layer

Purpose

Create an analytics-ready dimensional model.

### Dimension Tables

- dim_department
- dim_employee
- dim_supplier
- dim_product

### Fact Tables

- fact_purchase_requisition
- fact_purchase_order
- fact_goods_receipt
- fact_invoice
- fact_payment

---

# Audit Layer

The Audit schema stores records that require investigation.

Examples

- Duplicate Records
- Invalid Records
- ETL Execution Logs
- Data Quality Metrics

---

# Data Quality Checks

Every notebook performs:

- Record Count Validation
- Duplicate Detection
- Null Validation
- Data Type Validation
- Foreign Key Validation

---

# Coding Standards

The project follows industry best practices.

✔ Modular notebooks

✔ Reusable helper functions

✔ Configuration driven

✔ No hard-coded values

✔ Explicit schemas

✔ Delta tables

✔ Error handling

✔ Audit logging

✔ Data validation

✔ Production-style documentation

---

# Business Rules

Examples

Purchase Requisition

- Approval Lead Time
- Pending Approval Flag

Purchase Order

- Late Delivery
- Open Purchase Orders

Goods Receipt

- Receipt Variance

Invoices

- Invoice Aging

Payments

- Payment Delay

Supplier

- Supplier Performance

---

# Power BI Dashboard

The dashboard includes

- Executive Summary
- Procurement KPIs
- Purchase Orders
- Supplier Performance
- Invoice Analysis
- Payment Analysis
- Goods Receipt Analysis

---

# Key Features

- End-to-End ETL Pipeline
- Medallion Architecture
- Delta Lake
- Data Quality Framework
- Audit Framework
- Duplicate Detection
- Reusable Helper Functions
- Power BI Dashboard
- GitHub Version Control

---

# Future Enhancements

- Incremental Data Loading
- Slowly Changing Dimensions (SCD Type 2)
- Delta Merge Operations
- Parameterized Pipelines
- Unit Testing
- CI/CD
- Azure Data Factory Integration
- Microsoft Fabric Migration

---

# Learning Outcomes

This project demonstrates practical experience with:

- Databricks
- PySpark
- Delta Lake
- Unity Catalog
- Data Engineering
- ETL Development
- Data Validation
- Data Quality
- Star Schema Design
- Power BI
- GitHub
- SQL

---

# Author

**V R Mutyala**

Power BI Developer | Azure Data Engineer | Databricks | PySpark | SQL | Microsoft Fabric

---

# License

This project is intended for educational and portfolio purposes.
