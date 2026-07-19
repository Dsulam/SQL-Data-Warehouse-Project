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

-SQL Development
-Data Architect
-Data Engineering
-ETL Pipeline Developer
-Data Modeling
-Data Analytics

🛠️ Important Links & Tools:
Everything is for Free!

Datasets: Access to the project dataset (csv files).
SQL Server Express: Lightweight server for hosting your SQL database.
SQL Server Management Studio (SSMS): GUI for managing and interacting with databases.
Git Repository: Set up a GitHub account and repository to manage, version, and collaborate on your code efficiently.
DrawIO: Design data architecture, models, flows, and diagrams.

🚀 Project Requirements
Building the Data Warehouse (Data Engineering)
Objective
Develop a modern data warehouse using SQL Server to consolidate sales data, enabling analytical reporting and informed decision-making.

Specifications
Data Sources: Import data from two source systems (ERP and CRM) provided as CSV files.
Data Quality: Cleanse and resolve data quality issues prior to analysis.
Integration: Combine both sources into a single, user-friendly data model designed for analytical queries.
Scope: Focus on the latest dataset only; historization of data is not required.
Documentation: Provide clear documentation of the data model to support both business stakeholders and analytics teams.

BI: Analytics & Reporting (Data Analysis)
Objective
Develop SQL-based analytics to deliver detailed insights into:

Customer Behavior
Product Performance
Sales Trends
These insights empower stakeholders with key business metrics, enabling strategic decision-making.




