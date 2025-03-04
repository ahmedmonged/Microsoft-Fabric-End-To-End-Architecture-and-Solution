# End-to-End Architecture and Solution Using Microsoft Fabric

### Brief Walkthrough Video

[![Microsoft Fabric End-To-End Architecture & Solution](https://ytcards.demolab.com/?id=zMvgg2BRlOY&title=Microsoft+Fabric+End-To-End+Architecture+%26+Solution&lang=en&timestamp=1737729650&background_color=%230d1117&title_color=%23ffffff&stats_color=%23dedede&max_title_lines=2&width=500&border_radius=10)](https://www.youtube.com/watch?v=zMvgg2BRlOY)


## Overview
This project aims to build an end-to-end data architecture and solution using Microsoft Fabric. The solution will ingest data from three different sources:
- **API**
- **On-premises systems**
- **Data Lake**

We will implement the Medallion Architecture for the enterprise and automate the entire process, ensuring that data is ingested and processed efficiently. The architecture will leverage pipelines for daily updates to the lakehouses and warehouses, with data being added incrementally.

## Architecture Diagram

![Architecture Diagram](img/arhitdesginmedallionFabric.jpg)

### Medallion Architecture
The Medallion Architecture in this solution is designed as follows:
- **Bronze Layer**: Raw data is ingested and stored in a Lakehouse.
- **Silver Layer**: Cleaned and transformed data is stored in another Lakehouse.
- **Gold Layer**: Refined data stored in a multitable warehouse, supporting multiple departments and domains.

### Ingestion & Data Processing
- **API**: Data will be ingested from external APIs.
- **On-Premises**: Data will be ingested from on-premises systems.
- **Data Lake**: Data will be sourced from the existing data lake.

We will process and manage large-scale data using **PySpark** in notebooks, taking advantage of the powerful capabilities of Microsoft Fabric for processing and scaling.

### Incremental Loading
The solution will implement **incremental loading** to ensure only new or changed data is processed, optimizing performance and minimizing resource usage.

### Automation with Pipelines
We will automate the entire process using **pipelines**, ensuring that data is continuously added to the lakehouses and warehouses on a daily basis. This will include automated data transformations and loading to the various layers.

### Error Handling and Logging
We will log actions and handle any errors that may arise during the process. This includes:
- **Error Notifications**: Notifications will be sent if any errors occur.
- **Action Logging**: All actions will be logged for debugging and tracing issues.

## Final Data Consumption

Once the data is processed and refined through the Medallion Architecture, it will feed into multiple **dashboards**. These dashboards will be scheduled to refresh regularly, ensuring that business users have access to up-to-date data to make informed, data-driven decisions.

## Conclusion
This project leverages the power of Microsoft Fabric to automate and scale data processing while ensuring a smooth flow from raw data ingestion to actionable insights. With the Medallion Architecture, automated pipelines, and robust error handling, this solution is designed to support business intelligence and decision-making at the enterprise level.
