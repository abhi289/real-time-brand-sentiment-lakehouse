# Real-time Social Media Sentiment Analysis Pipeline

## Project Overview
End-to-end data engineering pipeline processing 1.5M+ tweets to analyze brand sentiment for major tech companies.


## Technology Stack
- **Databricks**: Unified analytics platform
- **PySpark**: Distributed data processing
- **Delta Lake**: Reliable data storage with ACID transactions
- **Databricks SQL**: Visualization and dashboarding

## Pipeline Steps

### 1. Data Ingestion (Bronze Layer)
- Used AutoLoader with Trigger.AvailableNow for efficient ingestion
- Processed 1.52M records from CSV source

### 2. Data Transformation (Silver Layer)
- Text cleaning: removed URLs, special characters, normalized case
- Schema enforcement and data quality checks

### 3. Sentiment Analysis (Gold Layer)
- Brand detection using custom UDF with keyword dictionary
- Aggregated sentiment counts by brand
- Processed 1.52M records in ~4 minutes

### 4. Visualization
- Interactive Databricks SQL Dashboard
- Real-time sentiment monitoring by brand
![](/Workspace/Users/ajagtap289@gmail.com/real-time-brand-sentiment-lakehouse/Dashboard.JPG)

## How to Run
1. Set up Databricks workspace
2. Create cluster with Delta Lake support
3. Run notebooks in sequence: 01_ingestion → 02_transformation → 03_analysis
4. Create SQL dashboard using provided queries

