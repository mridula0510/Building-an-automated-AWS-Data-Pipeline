# Data Engineering Platform: Data Warehouse + Cloud Data Lake

## Overview

Welcome to the Data Engineering Platform repository.

This project demonstrates an end-to-end data engineering solution that combines a Modern SQL Data Warehouse with a Cloud-Based Data Lake Architecture. The platform integrates enterprise data from multiple source systems, applies data quality and transformation processes, and delivers analytics-ready datasets for business intelligence and reporting.

The project is implemented in two phases:

### Phase 1 – Modern SQL Data Warehouse

A SQL Server-based Data Warehouse built using Medallion Architecture (Bronze, Silver, Gold) for structured data integration, transformation, and analytics.

### Phase 2 – Cloud Data Lake & Analytics Platform

A cloud-native architecture utilizing AWS Glue, Amazon S3, Amazon SNS, Amazon SQS, Snowflake, Snowpipe, Amazon Athena, and Tableau for scalable storage, automated ingestion, and enterprise analytics.

---

# Data Architecture

The project follows a Medallion Architecture across both the SQL Warehouse and Snowflake environments.

## Bronze Layer

Stores raw source data without modification.

* Raw ERP and CRM datasets
* Data ingestion through SQL ETL and AWS Glue
* Historical traceability and auditing

## Silver Layer

Applies data quality and transformation rules.

* Data cleansing
* Standardization
* Deduplication
* Validation
* Business rule implementation

## Gold Layer

Provides business-ready analytical datasets.

* Fact tables
* Dimension tables
* Curated analytical views
* Reporting-ready models

---

# Cloud Architecture

The cloud platform extends the warehouse architecture through AWS and Snowflake services.

Source Systems
↓
AWS Glue ETL
↓
Amazon S3 Data Lake
↓
CDC Validation
↓
SNS Notification
↓
SQS Queue
↓
Snowpipe
↓
Snowflake (Bronze → Silver → Gold)
↓
Athena / Tableau

---

# Project Overview

This project involves:

### Data Engineering

* Designing a Modern SQL Data Warehouse
* Building ETL pipelines
* Implementing Medallion Architecture
* Data quality validation
* Dimensional modeling

### Cloud Data Engineering

* AWS Glue ETL processing
* Amazon S3 Data Lake implementation
* Event-driven architecture using SNS and SQS
* Snowpipe auto-ingestion
* Snowflake data transformation
* Athena-based querying

### Analytics & Reporting

* Customer Analytics
* Product Analytics
* Sales Analytics
* KPI Reporting
* Tableau Dashboards

---

# Technologies Used

## Data Warehouse

* SQL Server Express
* SQL Server Management Studio (SSMS)
* T-SQL
* CSV Data Sources

## Cloud Platform

* AWS Glue
* Amazon S3
* Amazon SNS
* Amazon SQS
* Snowflake
* Snowpipe
* Amazon Athena

## Visualization

* Tableau

## Documentation & Version Control

* DrawIO
* GitHub

---

# Project Requirements

## Phase 1 – SQL Data Warehouse

### Objective

Develop a modern SQL Data Warehouse to consolidate ERP and CRM data for analytical reporting and business intelligence.

### Scope

* Data ingestion from ERP and CRM systems
* Data cleansing and transformation
* Star schema implementation
* Analytical querying

---

## Phase 2 – Cloud Data Lake

### Objective

Build a scalable cloud-based Data Lake and analytics platform using AWS and Snowflake technologies.

### Scope

* JDBC-based data extraction
* AWS Glue ETL processing
* Amazon S3 storage
* CDC implementation
* SNS and SQS event processing
* Snowpipe auto-ingestion
* Snowflake transformations
* Athena analytics
* Tableau reporting

---

# Repository Structure

data-engineering-platform/

├── datasets/
│
├── docs/
│   ├── architecture/
│   ├── data_models/
│   ├── flow_diagrams/
│   └── data_catalog/
│
├── phase-1-sql-data-warehouse/
│   ├── bronze/
│   ├── silver/
│   ├── gold/
│   └── analytics/
│
│
├── tests/
│
├── README.md
├── LICENSE
└── .gitignore

---

# Key Features

* End-to-End Data Engineering Pipeline
* Medallion Architecture Implementation
* SQL Data Warehouse Development
* Cloud Data Lake Architecture
* Automated ETL Pipelines
* Event-Driven Data Processing
* Snowflake Analytics Platform
* Tableau Reporting Integration
* Enterprise Data Quality Framework

---

# Business Outcomes

* Improved Data Quality
* Centralized Analytics Platform
* Automated Data Processing
* Faster Reporting
* Scalable Cloud Architecture
* Business-Ready Analytical Models
* Enhanced Decision Making

---
