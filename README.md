# Real-time Data Processing with Azure Databricks

This repository contains a notebook demonstrating the architecture for building real-time data pipelines using Azure Databricks.

## Overview

- **Data Sources**: Streaming data from various sources.
- **Ingestion**: Utilizing Azure Event Hubs for capturing real-time data.
- **Processing**: Leveraging Azure Databricks for stream processing using Structured Streaming.
- **Storage**: Storing processed data in Azure Data Lake (Delta Format).
- **Visualization**: Visualizing data using Power BI.

## Medallion Architecture

- This is a **data design pattern** used to organize data in a lakehouse to incrementally improve the structure & quality of data as it flows through each layer.
- Also known as 'multi-hop' architecture.
- Layers in the architecture:
1. **Bronze Layer**: Serves as the initial landing zone for data from external sources,
2. **Silver Layer**: Define the schema, transform data from the bronze to the silver layer, and write it.
3. **Gold Layer**: Aggregate data from the silver layer, perform calculations, and store aggregated data in consumption-ready form.

## Sample Data

```json
{
    "temperature": 20,
    "humidity": 60,
    "windSpeed": 10,
    "windDirection": "NW",
    "precipitation": 0,
    "conditions": "Partly Cloudy"
}
```