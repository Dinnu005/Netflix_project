# Netflix Data Engineering Project (Azure Lakehouse)

## Overview
This project implements an end-to-end cloud-based data engineering pipeline using Azure services.
The solution ingests raw Netflix-style datasets, processes them through a modern lakehouse
architecture, and prepares analytics-ready data for reporting and downstream consumption.

The project follows industry best practices including scalable ingestion, layered data architecture,
and centralized governance.

---

## Architecture
The pipeline follows a Bronze–Silver–Gold lakehouse pattern.

**Data Flow:**
- Source: GitHub-hosted CSV datasets
- Ingestion: Azure Data Factory (ADF)
- Storage: Azure Data Lake Storage Gen2 (ADLS)
- Processing: Azure Databricks
- Governance: Unity Catalog
- Analytics: Power BI / Azure Synapse

![Architecture]
<img width="1024" height="572" alt="image" src="https://github.com/user-attachments/assets/24097b22-4f2b-4449-ae59-1bdc943d52f8" />


## Implementation Details

### Data Ingestion
- Built a dynamic Azure Data Factory pipeline to ingest multiple datasets from GitHub
- Implemented parameterized datasets and ForEach activity for scalable ingestion
- Added validation and monitoring for reliable pipeline execution

### Data Storage
- Designed and implemented a Bronze layer in ADLS Gen2 for raw data storage
- Structured the data lake using lakehouse best practices

### Data Processing
- Configured Azure Databricks for data transformation
- Applied Bronze to Silver transformations including data cleansing and normalization
- Created analytics-ready datasets following a Gold layer star schema design

### Governance
- Configured Unity Catalog metastore for centralized data governance
- Enabled structured data access and metadata management

---

## Tech Stack
- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure Databricks
- Unity Catalog
- GitHub
- Power BI / Azure Synapse
