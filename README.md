# End-to-End SQL Data Warehouse Project

An end-to-end SQL Data Warehouse solution built from raw transactional source data to a production-ready Star Schema. This project showcases data extraction, staging transformations, dimensional modeling (Kimball methodology), data quality testing, and analytics-ready reporting views.

---

## Executive Summary & Architecture

The goal of this project is to consolidate fragmented operational data into a centralized, highly performant data warehouse to support business intelligence and executive decision-making.

Data Flow:
Raw Source Data -> Bronze / Staging Layer (Raw Ingestion) -> Silver / Intermediate Layer (Data Cleaning & Quality Checks) -> Gold / Data Warehouse Layer (Star Schema Model) -> Analytics & BI Views

---

## Tech Stack & Skills

* Database Engine: PostgreSQL / Snowflake / MS SQL Server
* Data Modeling: Kimball Methodology (Star Schema, Surrogate Keys, SCD)
* SQL Techniques: CTEs, Window Functions, Stored Procedures, Constraints
* Analytics: SQL Analytical Queries & Executive Views

---

## Dimensional Data Model (Star Schema)

The warehouse uses a star schema structure centered around key business metrics, optimized for fast analytical querying.

Fact Tables:
* fact_sales: Contains transactional metrics (units sold, net amount, discount, tax).

Dimension Tables:
* dim_customer: Customer demographic and location data.
* dim_product: Product hierarchy, categorization, and pricing history.
* dim_date: Comprehensive date dimension for time-series analysis.

---

## Repository Structure

datasets/ - Sample datasets or data generation scripts
scripts/
  01_bronze_staging.sql - Table creation for raw data loading
  02_silver_cleaning.sql - Transformation, casting, and data quality checks
  03_gold_star_schema.sql - Fact & Dimension schema logic
  04_analytics_views.sql - Executive views & KPI queries
tests/ - Data quality assertion scripts
LICENSE
README.md

---

## Key Pipeline Steps

1. Raw Data Ingestion (Bronze): Raw file loading without altering source values.
2. Data Cleaning & Transformation (Silver): Missing value handling, deduplication, and schema standardization.
3. Star Schema Modeling (Gold): Generating surrogate keys, handling dimension changes, and constructing fact tables.

---

## How to Run

1. Clone the repository:
   git clone https://github.com/your-username/sql-data-warehouse-project.git
2. Navigate to directory:
   cd sql-data-warehouse-project
3. Run SQL scripts in numerical order (01 through 04) inside your SQL editor.

---

## License

Distributed under the MIT License. See LICENSE for more details.
