# SQL Data Warehouse — CRM & ERP Integration

An end-to-end data warehouse built in SQL Server, consolidating customer,
product, and sales data from two source systems (CRM and ERP) into an
analytics-ready star schema. Built to practice data engineering fundamentals:
ETL, data quality, integration, and dimensional modeling.

<img width="1740" height="1306" alt="image" src="https://github.com/user-attachments/assets/9fa9dbd0-a5b5-4aac-9d37-664bcdbbec64" />


## 🏗️ Data Architecture

The warehouse follows a three-layer medallion architecture:

- **Bronze** — Raw data ingested as-is from CRM and ERP source files. No transformation.
- **Silver** — Cleansed and standardized: null handling, type casting, deduplication,
  value normalization, and key alignment across systems.
- **Gold** — Business-ready star schema (fact and dimension tables) for reporting.

---

## 📖 Project Overview


This project involves:

Data Architecture: Designing a Modern Data Warehouse Using Medallion Architecture Bronze, Silver, and Gold layers.
ETL Pipelines: Extracting, transforming, and loading data from source systems into the warehouse.
Data Modeling: Developing fact and dimension tables optimized for analytical queries.
Analytics & Reporting: Creating SQL-based reports and dashboards for actionable insights.
🎯 This repository is an excellent resource for professionals and students looking to showcase expertise in:

SQL Development
Data Architect
Data Engineering
ETL Pipeline Developer
Data Modeling
Data Analytics

- **ETL pipelines** — Stored procedures that truncate and reload each layer,
  with per-table load logging and TRY/CATCH error handling.
- **Data quality** — Automated checks for null and duplicate primary keys.
  Deduplication with `ROW_NUMBER()` to retain the most recent record per entity.
- **Integration** — Reconciled mismatched customer/product keys between CRM and ERP
  (prefix stripping, delimiter normalization) so the two systems join cleanly.
- **Data modeling** — Gold layer modeled as a star schema: `fact_sales` with
  conformed `dim_customers` and `dim_products` dimensions.

---

## Data Quality Highlights

- Detected and removed duplicate and null primary keys in the customer table
  (6 problem keys in source → 0 after cleansing).
- Standardized categorical values (gender, marital status, country, product line)
  from raw source codes to readable, consistent labels.
- Recalculated invalid sales figures and derived missing prices from
  quantity × price logic.
- Resolved gender conflicts between CRM and ERP using CRM as the source of truth.

---

## Project Status

- [x] Bronze layer — raw ingestion
- [x] Silver layer — cleansing, deduplication, integration
- [x] Gold layer — star schema (in progress)

---

## Tech Stack

- SQL Server / T-SQL
- SQL Server Management Studio (SSMS)
- Medallion architecture (Bronze / Silver / Gold)
- Star schema dimensional modeling

---

## Repository Structure


