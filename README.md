# AWS-Based Data Pipeline for COVID-19 Analysis 🦠☁️

This project demonstrates a fully automated ETL pipeline to ingest, process, and load COVID-19-related data using AWS services and Python scripting.

## 📌 Architecture Overview

**Flow:**  
Source Data ➝ Amazon S3 ➝ Amazon Athena ➝ AWS Glue (Python Script) ➝ Amazon Redshift

<p align="center">
  <img src="https://github.com/user-attachments/assets/7eea2ee6-d03b-4d79-b669-18948f098b15" alt="Architecture Diagram" width="600"/>
</p>

## ⚙️ Workflow Summary

- **Athena Query Execution:** Connected to Amazon Athena using `boto3` to run SQL queries on COVID-19 data stored in S3.
- **DataFrame Transformation:** Loaded results into Pandas, performed merges to generate fact and dimension tables.
- **S3 Storage:** Exported final tables as CSVs and uploaded them to Amazon S3.
- **Schema Extraction:** Dynamically generated SQL schemas from DataFrames for Redshift.
- **Redshift Integration:** Created Redshift tables using `redshift_connector` and loaded data using the COPY command.

## 💡 Key Features

- Built using native AWS services for scalability and cost-efficiency.
- Handles end-to-end data ingestion, transformation, and warehousing.
- Automates schema generation and minimizes manual SQL writing.
- Ready for analytical workloads, BI dashboards, and reporting.

## 🧰 Tools Used

- AWS Athena
- AWS S3
- AWS Glue (Python script)
- Amazon Redshift
- Pandas · Boto3 · redshift_connector
