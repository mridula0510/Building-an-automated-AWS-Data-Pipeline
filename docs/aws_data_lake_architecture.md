# Phase 2 - Cloud Data Lake Architecture

## Overview

To extend the capabilities of the SQL Data Warehouse, the project was enhanced with a cloud-based Data Lake architecture built using AWS and Snowflake technologies. This phase focuses on scalable data storage, automated data ingestion, cloud-native processing, and analytical reporting.

The cloud architecture demonstrates how modern organizations process large volumes of data efficiently while maintaining data quality, governance, and performance. By integrating AWS services with Snowflake, the solution enables automated movement of data from source systems to analytics-ready datasets.

---

## Architecture Flow

```text
Source Systems
      ↓
AWS Glue
      ↓
Amazon S3 Data Lake
      ↓
SNS Notification Service
      ↓
SQS Message Queue
      ↓
Snowpipe Auto-Ingestion
      ↓
Snowflake (Bronze → Silver → Gold)
      ↓
Athena / Tableau
```

---

## Component Overview

### AWS Glue

AWS Glue is a serverless ETL (Extract, Transform, Load) service used to automate data ingestion and transformation processes. It connects to source systems through JDBC connections, extracts data, performs preprocessing tasks, and loads the resulting datasets into the Data Lake.

### Amazon S3

Amazon S3 serves as the central Data Lake storage layer. It stores both raw and processed datasets in a scalable and cost-effective manner while supporting downstream analytics and reporting workloads.

### Amazon SNS (Simple Notification Service)

Amazon SNS provides event-driven notifications whenever new files arrive in the Data Lake. These notifications help automate downstream processing activities without requiring manual intervention.

### Amazon SQS (Simple Queue Service)

Amazon SQS acts as a reliable messaging layer between services. It receives notifications from SNS and ensures that ingestion requests are processed efficiently and without data loss.

### Snowpipe

Snowpipe is Snowflake's continuous data ingestion service. It automatically detects new files in Amazon S3 and loads them into Snowflake, enabling near real-time data availability.

### Snowflake

Snowflake is the cloud data platform used for storing, transforming, and analyzing data. The platform follows the Medallion Architecture approach:

- **Bronze Layer** – Raw ingested data
- **Silver Layer** – Cleaned and standardized data
- **Gold Layer** – Business-ready analytical datasets

This layered design improves maintainability, data quality, and analytical performance.

### Amazon Athena

Amazon Athena provides serverless SQL querying capabilities directly on data stored in Amazon S3. It is used for validation, ad-hoc analysis, and exploratory querying of Data Lake datasets.

### Tableau

Tableau serves as the visualization and reporting layer. Curated datasets from Snowflake are used to create dashboards, KPI reports, trend analysis, and business intelligence solutions.

---

## Key Concepts Demonstrated

- Data Lake Architecture
- ETL and ELT Processing
- Cloud Data Engineering
- Event-Driven Data Pipelines
- Automated Data Ingestion
- Medallion Architecture
- Data Warehousing on Snowflake
- Serverless Analytics
- Business Intelligence and Reporting

---

## Learning Outcomes

Through this implementation, the project demonstrates practical understanding of modern data engineering concepts including cloud-based storage, ETL automation, event-driven architectures, scalable analytics platforms, and enterprise reporting solutions. The architecture showcases how traditional data warehousing principles can be extended using cloud-native technologies to support modern analytical workloads.

---


