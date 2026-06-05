# Phase 2 - Cloud Data Lake Architecture

## Overview
This phase extends the SQL Data Warehouse by introducing a cloud-based
data lake architecture for scalable storage, automated ingestion,
and analytical processing.

## Architecture

Source Systems
    ↓
AWS Glue
    ↓
Amazon S3
    ↓
CDC Validation
    ↓
SNS
    ↓
SQS
    ↓
Snowpipe
    ↓
Snowflake
    ↓
Athena / Tableau

## Technologies Used

- AWS Glue
- Amazon S3
- Amazon SNS
- Amazon SQS
- Snowflake
- Snowpipe
- Amazon Athena
- Tableau

## Key Responsibilities

- Data ingestion automation
- Data lake storage
- Event-driven processing
- Automated Snowflake loading
- Data transformation
- Reporting and analytics

## Note

This repository contains a conceptual implementation only.
Production code, cloud resources, configurations, credentials,
and business-specific logic are excluded due to confidentiality
requirements.
