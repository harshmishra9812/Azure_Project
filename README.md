# Data Source
The data source for this project is raw data collected from various external sources and ingested into the Azure environment.
This raw data forms the foundation for further processing and analysis in the pipeline.

# Data Ingestion Using Azure Data Factory

Azure Data Factory (ADF) is used to orchestrate the data ingestion process. It automates the extraction of raw data from external sources and loads it into Azure Data Lake Gen2 for storage.
  # Implementation Steps:

Create Linked Services: Set up linked services in ADF to connect to the source data and destination storage in Azure Data Lake Gen2.
Define Datasets: Create datasets in ADF representing both the input (raw data) and output (ingested data) formats.
Create Pipelines: Design pipelines that use Copy Activity to move data from source to the Bronze Layer in ADLS Gen2. This ensures scheduled, repeatable, and monitored data ingestion.

