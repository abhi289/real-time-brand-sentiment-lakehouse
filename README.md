# 🌐 Real-Time Social Media Sentiment Analysis Pipeline

## 📊 Project Overview
An end-to-end data engineering pipeline processing **1.5M+ tweets** to perform multi-dimensional sentiment analysis for major tech brands across geographic, demographic, and temporal dimensions.

## 🏗️ Architecture
![![Pipeline Architecture](images/architecture_diagram.png)](Architecture And Results/Architecture Diagram.JPG)

**Medallion Architecture Implementation:**
- **Bronze Layer**: Raw data ingestion using Databricks AutoLoader
- **Silver Layer**: Data cleaning, text processing, and brand detection
- **Gold Layer**: Aggregated tables for dashboarding and analysis

## 🛠️ Technology Stack
- **Databricks**: Unified analytics platform with Delta Lake
- **PySpark**: Distributed data processing (1.5M records processed in ~4 minutes)
- **Delta Lake**: ACID transactions, time travel, and schema enforcement
- **Databricks SQL**: Interactive dashboarding and visualization
- **Unity Catalog**: Data governance and management

## 📈 Key Features

### Data Processing
- **Scalable Ingestion**: AutoLoader with Trigger.AvailableNow pattern
- **Advanced Text Cleaning**: URL removal, special character handling, normalization
- **Brand Detection**: Custom UDF detecting 5+ tech brands (Apple, Google, Microsoft, Samsung, Amazon)
- **Multi-dimensional Analysis**: Sentiment across countries, age groups, and time periods

### Analytics & Insights
- **Global Heatmaps**: Sentiment distribution across 50+ countries
- **Demographic Analysis**: Age-based sentiment patterns (0-20, 21-30, 31-45, 46-60, 60-70, 70-100)
- **Temporal Patterns**: Time-of-day sentiment variations (morning, noon, night)
- **Competitive Intelligence**: Cross-brand sentiment comparison

## 🚀 Pipeline Steps

### 1. Data Ingestion (Bronze Layer)
- Automated data ingestion using Databricks AutoLoader
- Processed 1.52M records from multiple datasets
- Unity Catalog volumes for cloud-agnostic storage

### 2. Data Transformation (Silver Layer)
- Text preprocessing, cleaning and transformations
- Brand detection using custom PySpark UDFs
- Schema enforcement and data quality checks

### 3. Sentiment Analysis (Gold Layer)
- Multi-dimensional aggregation by brand, country, age group, and time
- Sentiment scoring and percentage calculations
- Optimized Delta tables for dashboard performance

### 4. Visualization & Dashboarding
- Interactive Databricks SQL dashboard
- Real-time sentiment monitoring
- Geographic heatmaps and demographic analysis

## 📊 Sample Insights
- **Geographic Trends**: Country-specific sentiment patterns for each brand
- **Age Preferences**: How different age groups perceive tech brands
- **Optimal Timing**: Best times for positive social media engagement
- **Competitive Analysis**: Relative brand perception across markets

## 🏆 Business Impact
This pipeline transforms raw social data into actionable business intelligence:
- **Marketing Optimization**: Target campaigns based on demographic sentiment
- **Crisis Detection**: Early warning system for PR issues
- **Competitive Intelligence**: Track brand perception vs. competitors
- **Global Expansion**: Identify most receptive markets for growth
- **Global Brand Monitoring**: Track how sentiment varies across different markets
- **Temporal Insights**: Identify optimal posting times for social media engagement

## 📈 Results
- **Processing Time**: 4 minutes for 1.5M records on single-node cluster
- **Brand Detection Accuracy**: Custom UDF with precise keyword matching
- **Dashboard Performance**: Sub-second query response on aggregated tables

## 🤝 Contributing
Feel free to fork this project and submit pull requests for:
- Additional data sources
- Enhanced brand detection algorithms
- New visualization types
- Performance optimizations

## 👨‍💻 Author
[Abhishek Jagtap]
- Data Engineer specializing in big data processing and analytics
- Connect with me on www.linkedin.com/in/abhishek-jagtap-0b0a73125
