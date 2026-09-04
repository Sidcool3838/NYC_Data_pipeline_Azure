# NYC_Data_pipeline_Azure
We hereby certify that the work being presented in the project report entitled "Enterprise Data Processing Pipeline with PySpark, SQL and Azure Cloud", in partial fulfillment of the requirements for the award of Post Graduate Diploma in Big Data Analytics (PG-DBDA), submitted to the Centre for Development of Advanced Computing (C-DAC), Bangalore.
# Project Name

## 📌 Project Overview

This project implements an end-to-end data engineering pipeline using
Azure Data Factory, Azure Data Lake Storage Gen2, Databricks, PySpark,
Delta Lake, and Azure SQL Database.

The pipeline ingests raw data from source systems, performs data
transformation and cleansing, and loads the processed data into
the target database for reporting and analytics.

---

## 🏗️ Architecture

The pipeline follows the architecture:

Source → ADF → ADLS Gen2 → Databricks → Delta Lake → Azure SQL → Power BI

### Architecture Components

- **Azure Data Factory** – Pipeline orchestration and data ingestion
- **ADLS Gen2** – Data lake storage
- **Azure Databricks** – Data processing
- **PySpark** – Data transformation
- **Delta Lake** – Reliable storage and processing
- **Azure SQL Database** – Serving layer
- **Power BI** – Reporting and visualization

---

## 🔄 Data Pipeline

1. ADF extracts data from the source system.
2. Raw files are stored in ADLS Gen2.
3. ADF triggers the Databricks notebook.
4. Databricks reads the raw data using PySpark.
5. Data cleansing and transformation are performed.
6. Transformed data is stored in Delta format.
7. Curated data is loaded into Azure SQL Database.
8. Power BI consumes the curated data for reporting.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Data processing and scripting |
| PySpark | Distributed data transformation |
| SQL | Data querying and validation |
| Azure Data Factory | Pipeline orchestration |
| ADLS Gen2 | Data storage |
| Databricks | Data processing |
| Delta Lake | Data storage and ACID transactions |
| Azure SQL | Target database |
| Power BI | Visualization |

---

## 📂 Repository Structure

```text
project-name/
│
├── notebooks/
│   ├── ingestion.py
│   ├── transformation.py
│   └── loading.py
│
├── adf/
│   ├── pipelines/
│   ├── datasets/
│   └── linked-services/
│
├── sql/
│   ├── create_tables.sql
│   └── validation_queries.sql
│
├── config/
│   └── config.json
│
├── tests/
│   └── test_transformations.py
│
├── README.md
└── requirements.txt
