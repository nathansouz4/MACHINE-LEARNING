
# Chapter 3: Data Engineering Fundamentals

## Overview
- The rise of Machine Learning (ML) has grown alongside big data, making data engineering essential for building ML systems.
- This chapter covers the basics of data sources, formats, models, storage, processing, and dataflow modes critical to ML system design.

## Key Topics 

## 1. Data Sources
- **User Input Data**: Directly from users, often requires immediate processing and validation (e.g., text, images).
- **System-Generated Data**: Logs and system outputs, primarily used for debugging and monitoring.
- **User Behavior Data**: Records actions like clicks, scrolls, etc., often subject to privacy concerns.
- **Internal Databases**: Company data on inventory, customer relationships, etc.
- **Third-Party Data**: Data from external sources, usually purchased, helps with user insights but increasingly restricted due to privacy regulations.

## 2. Data Formats
- **Common Formats**:
  - **JSON**: Text-based, human-readable, widely used for semi-structured data.
  - **CSV**: Row-major format, simple but lacks flexibility.
  - **Parquet**: Column-major, binary format optimized for analytical processing, saves storage space.
- **Row-Major vs. Column-Major**:
  - Row-major formats (e.g., CSV) are better for writing and accessing rows.
  - Column-major formats (e.g., Parquet) are optimal for column-based analytics.

## 3. Data Models
- **Relational Model**: Organizes data in tables, suited for structured data and joins. Commonly used with SQL.
- **Document Model**: Stores data in self-contained documents (JSON, BSON), supports flexible schemas.
- **Graph Model**: Represents data with nodes and edges, prioritizes relationships, ideal for social network structures.

## 4. Structured vs. Unstructured Data
- **Structured Data**: Follows a schema, easier to analyze but less flexible.
- **Unstructured Data**: Schema-less, adaptable to changing data types but can be challenging for analysis.
- **Data Lakes vs. Data Warehouses**:
  - **Data Lakes**: Store raw, unstructured data.
  - **Data Warehouses**: Store processed, structured data ready for analysis.

     <img src="images/structured x unstructured data.jpg" alt="ML system Overview" style="display: block; margin-left: auto; margin-right: auto;">

## 5. Data Storage Engines and Processing
- **Transactional Databases (OLTP)**: Process online transactions with ACID properties (atomicity, consistency, isolation, durability), optimized for low-latency processing.
- **Analytical Databases (OLAP)**: Process large-scale analytics, optimized for column-based aggregation.

## 6. ETL (Extract, Transform, Load)
- **Extract**: Pulls data from multiple sources.
- **Transform**: Cleans, joins, and standardizes data.
- **Load**: Saves the data in a target storage, often a database or data warehouse.
- **ETL vs. ELT**:
  - ETL performs transformation before loading.
  - ELT loads data first (often into a data lake) and transforms later, enabling faster data intake.

## 7. Modes of Dataflow
- **Data Passing Through Databases**: Simple but can be slow, suitable for non-real-time data.
- **Data Passing Through Services**: Uses REST or RPC to request data between services, ideal for real-time needs.
- **Data Passing Through Real-Time Transport**:
  - Utilizes tools like Apache Kafka to facilitate asynchronous, low-latency data flow.
  - **Event-Driven Architecture**: Services publish data to a broker, which is accessed by subscribing services.

## 8. Batch Processing vs. Stream Processing
- **Batch Processing**: Processes historical data periodically, generating **static features** (e.g., user ratings).
- **Stream Processing**: Works on real-time data, creating **dynamic features** (e.g., current availability), often requires stream computation engines like Apache Flink.

## Conclusion
- Choosing appropriate data formats, models, storage, and processing methods is critical to the success of ML systems.
- As data complexity grows, modern systems may combine traditional batch processing with streaming data processing to handle diverse use cases.
