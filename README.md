# sql-data-warehouse-project
Building a modern data warehouse with sql server , including ETL process , data modeling and analytics. 

# 📊 SQL Data Warehouse and Analytics Project

Welcome to the **SQL Data Warehouse and Analytics Project** 🚀

This project demonstrates how to build a modern data warehouse using **SQL Server**, starting from raw data sources and transforming them into a clean, structured data model that can be used for analytical reporting and business insights.

The project covers the complete data warehousing process:

**Data Sources → Data Cleaning → Data Transformation → Data Warehouse → Analytics**

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Business Problem](#-business-problem)
- [Project Objectives](#-project-objectives)
- [Data Sources](#-data-sources)
- [Data Warehouse Architecture](#-data-warehouse-architecture)
- [Data Layers](#-data-layers)
- [Data Integration](#-data-integration)
- [Data Quality](#-data-quality)
- [Data Model](#-data-model)
- [Analytics and Reporting](#-analytics-and-reporting)
- [Key Business Questions](#-key-business-questions)
- [Technologies Used](#-technologies-used)
- [Project Structure](#-project-structure)
- [ETL Process](#-etl-process)
- [How to Run the Project](#-how-to-run-the-project)
- [Project Outcomes](#-project-outcomes)
- [Future Improvements](#-future-improvements)
- [Author](#-author)

---

# 📖 Project Overview

The goal of this project is to develop a **modern data warehouse using SQL Server** that consolidates sales-related data from multiple source systems.

The project uses data from two different source systems:

- ERP (Enterprise Resource Planning)
- CRM (Customer Relationship Management)

The source data is provided in **CSV files**.

The data is extracted, cleaned, transformed, integrated, and stored in a centralized data warehouse.

The final warehouse provides a reliable foundation for analytical queries and reporting.

---

# 💼 Business Problem

Organizations often store their business data across multiple systems.

For example:

- Customer information may exist in a CRM system.
- Product information may exist in an ERP system.
- Sales transactions may be stored in another system.

This creates several problems:

- Duplicate data
- Missing values
- Inconsistent formats
- Different naming conventions
- Difficult reporting
- Difficult data analysis
- Lack of a single source of truth

The purpose of this project is to solve these problems by creating a centralized **SQL Server Data Warehouse**.

---

# 🎯 Project Objectives

The main objectives of this project are:

### 1. Build a Data Warehouse

Develop a centralized data warehouse using SQL Server.

### 2. Integrate Multiple Data Sources

Combine data from ERP and CRM systems into a single analytical environment.

### 3. Improve Data Quality

Identify and resolve issues such as:

- Missing values
- Duplicate records
- Invalid values
- Inconsistent formats
- Incorrect data types

### 4. Create a User-Friendly Data Model

Design a data model that is easy for analysts and business users to query.

### 5. Enable Business Analytics

Use SQL to generate insights related to:

- Customer behavior
- Product performance
- Sales trends

### 6. Provide Documentation

Document the data architecture, data model, transformation process, and analytical queries.

---

# 📂 Data Sources

The project uses data from two source systems.

## ERP

The ERP system provides business and operational information such as:

- Customer information
- Product information
- Sales transactions
- Product categories
- Other operational data

## CRM

The CRM system provides customer-related information such as:

- Customer details
- Customer demographics
- Customer identifiers
- Customer-related information

The source data is provided in **CSV format**.

---

# 🏗️ Data Warehouse Architecture

The project follows a layered data warehouse architecture.

```text
                 ┌───────────────────┐
                 │    ERP CSV Files  │
                 └─────────┬─────────┘
                           │
                           │
                           ▼
                 ┌───────────────────┐
                 │   CRM CSV Files   │
                 └─────────┬─────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │  Bronze Layer   │
                  │  Raw Data       │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │  Silver Layer   │
                  │ Cleaned Data    │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │   Gold Layer    │
                  │ Business Model  │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │    Analytics    │
                  │  & Reporting    │
                  └─────────────────┘
