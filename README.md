# sql-data-warehouse-project_v2
Project Overview

This project demonstrates the end-to-end development of a SQL-based data warehouse using data sourced from two enterprise systems: ERP (Enterprise Resource Planning) and CRM (Customer Relationship Management). The source data is provided as CSV files and processed through a structured ETL (Extract, Transform, Load) pipeline following the Medallion Architecture.

Objectives

The primary objective of this project is to:

Extract data from ERP and CRM source systems.
Load raw CSV data into a SQL Server database.
Build a scalable data warehouse architecture using Bronze, Silver, and Gold layers.
Transform and cleanse data to improve quality and consistency.
Deliver business-ready analytical datasets using a dimensional model.
Data Warehouse Architecture
Bronze Layer - Raw Data Ingestion

The Bronze layer serves as the landing zone for raw data.

Data is loaded directly from CSV files located on the local machine.
SQL stored procedures are used to automate the data loading process.
Each source file is ingested into its corresponding database table without modifications.
This layer preserves the original source data for auditing and traceability purposes.
Silver Layer - Data Transformation and Cleansing

The Silver layer is responsible for refining the raw data.

Data is extracted from the Bronze layer.
Data quality issues are identified and corrected.
Records are cleaned, standardized, normalized, and transformed according to business requirements.
Invalid, duplicate, or inconsistent data is handled to ensure reliability.
This layer serves as the trusted and structured source for analytics.
Gold Layer - Business-Ready Data Models

The Gold layer contains curated datasets optimized for reporting and business intelligence.

Data is sourced from the Silver layer.
Information is organized using a Star Schema design.
Data is separated into:
Dimension tables containing descriptive attributes.
Fact tables containing measurable business metrics.
Relationships are established using primary and foreign keys to support efficient joins and analysis.
The Gold layer is implemented using SQL views rather than physical tables, providing a flexible and maintainable reporting layer.

ETL Process

This project implements a complete ETL pipeline:

Extract raw data from ERP and CRM CSV files.
Load the data into the Bronze layer.
Transform, clean, and normalize the data within the Silver layer.
Create analytical models in the Gold layer using dimensional modeling techniques.
Expose business-ready datasets through views for reporting and analytics.


Technologies Used
SQL Server
Stored Procedures
CSV Data Sources
ETL Processes
Medallion Architecture (Bronze, Silver, Gold)
Dimensional Modeling
Star Schema Design


Conclusion

This project showcases the implementation of a modern data warehousing solution using the Medallion Architecture. Raw data from multiple source systems is ingested, cleansed, transformed, and modeled into a well-structured analytical environment. The final Gold layer leverages a Star Schema composed of fact and dimension views, enabling efficient reporting, data analysis, and business intelligence workloads.
