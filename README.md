# SQL Data Warehouse — CRM & ERP Integration


Quick pause before I hand you text — because copying this one carries a real risk, and it's different from the resume bullets.
That README is Baraa's, and this is a known tutorial with 807 stars and 770k video views. If you copy his README verbatim into your own repo, two things happen. Recruiters who've seen the tutorial recognize it instantly — and a lot of data/supply-chain recruiters have. And it's got his name, YouTube links, PayPal, and newsletter all through it. Pasting that as-is reads as "I followed a tutorial and copied the README too," which undercuts the exact credibility the project is supposed to give you.
The MIT license means you may reuse it with attribution. But "allowed" and "helps you get hired" aren't the same thing here.
So rather than paste his text, let me give you a README written for your repo, in your voice, describing what you actually built. Same structure he taught you, none of the giveaways. This is genuinely better for you — and it's a thing an interviewer might ask about ("did you write this?"), so you want to be able to say yes.
Here it is, ready to paste into your own README.md:
markdown# SQL Data Warehouse — CRM & ERP Integration

An end-to-end data warehouse built in SQL Server, consolidating customer,
product, and sales data from two source systems (CRM and ERP) into an
analytics-ready star schema. Built to practice data engineering fundamentals:
ETL, data quality, integration, and dimensional modeling.

---

## Architecture

The warehouse follows a three-layer medallion architecture:

- **Bronze** — Raw data ingested as-is from CRM and ERP source files. No transformation.
- **Silver** — Cleansed and standardized: null handling, type casting, deduplication,
  value normalization, and key alignment across systems.
- **Gold** — Business-ready star schema (fact and dimension tables) for reporting.

---

## What This Project Covers

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

## Tech Stack

- SQL Server / T-SQL
- SQL Server Management Studio (SSMS)
- Medallion architecture (Bronze / Silver / Gold)
- Star schema dimensional modeling

---

## Repository Structure
