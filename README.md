## Project Overview
This project implements a scalable and robust Azure-based data pipeline for collecting, transforming, and visualizing data. It uses:

- **Azure Data Factory** for orchestrating data ingestion and transformation
- **Azure Data Lake Gen2** for storage (Bronze, Silver, Gold layers)
- **Mapping Data Flows** in ADF for data transformations
- **Power BI** for creating interactive dashboards

# Data Source
The data source for this project is raw data collected from **GitHub** and ingested into the Azure environment.  
This raw data forms the foundation for further processing and analysis in the pipeline.

## Data Ingestion Using Azure Data Factory
Azure Data Factory (ADF) automates the extraction of raw data and loads it into Azure Data Lake Gen2.

**Implementation Steps:**
1. **Create Linked Services**  
   Connect ADF to source data and Azure Data Lake Gen2.

2. **Define Datasets**  
   Represent both input (raw data) and output (processed data) formats.

3. **Create Pipelines**  
   Use **Copy Activity** to ingest data into the Bronze Layer, enabling scheduled, monitored, and repeatable data movement.

## Raw Data Storage (Bronze Layer)
The **Bronze Layer** stores raw, untransformed data in Azure Data Lake Gen2.

**Benefits of ADLS Gen2:**

- Hierarchical storage optimized for large datasets  
- Support for both structured and unstructured data  
- Integration with Azure analytics tools  
- Enterprise-grade security and governance

## Data Transformation (Silver Layer)
Data transformation is performed using **Mapping Data Flows** in Azure Data Factory.

**Key Capabilities:**

- Data cleansing, normalization, and enrichment  
- Filtering, joins, aggregations, and derived columns  
- Automatic scaling for large datasets

**Implementation Steps:**

1. **Create Data Flow**: Design a mapping data flow to process raw data  
2. **Transform Data**: Apply transformations like removing duplicates and handling missing values  
3. **Write to Gold Layer**: Store clean, structured data in the Gold Layer in ADLS Gen2

## Data Serving (Gold Layer)
The **Gold Layer** contains processed, analytics-ready data.

**Implementation Steps:**

1. **Connect Power BI**: Use DirectQuery or file-based connections to fetch Gold Layer data  
2. **Create Dashboards**: Build interactive reports and visualizations

---

## Reporting (Power BI)
Power BI is used to design dashboards and reports from the Gold Layer.

**Steps:**

1. **Connect to ADLS Gen2**: Access processed data files  
2. **Build Reports**: Create charts, tables, and visualizations for actionable insights

---

## Key Terminologies

- **ETL**: Extract, Transform, Load process for data integration  
- **Data Lake**: Central repository for raw and structured data  
- **Mapping Data Flow**: No-code tool in ADF for scalable data transformations  
- **Bronze, Silver, Gold Layers**: Standard layers for raw, cleaned, and transformed data  
- **DirectQuery**: Querying data directly without importing into Power BI
