# AW-Azure-Data-Engineering-Project
**📂 Azure Data Engineering Project: End-to-End Real-Time Pipeline**  

---

### **🔍 Overview**  
This project demonstrates a **production-grade data pipeline** on Azure, following the **Medallion Architecture** (Bronze → Silver → Gold layers). It ingests real-world sales data from APIs, transforms it using Spark, and serves analytics-ready data to stakeholders. Built to mirror industry scenarios, this project helped me crack data engineering interviews by showcasing hands-on expertise with Azure tools and solving real-time problems.  

---

### **🏗️ Architecture**  
1. **Bronze Layer (Raw Data)**:  
   - **Source**: AdventureWorks data pulled from GitHub APIs using **Azure Data Factory (ADF)**.  
   - **Storage**: Raw data stored in **Azure Data Lake Gen2** (CSV format).  

2. **Silver Layer (Cleaned/Transformed Data)**:  
   - **Transformation**: PySpark in **Azure Databricks** (date parsing, column splitting, aggregations).  
   - **Storage**: Processed data saved as Parquet files in Data Lake.  

3. **Gold Layer (Serving Layer)**:  
   - **Data Warehouse**: Structured tables in **Azure Synapse Analytics** for BI/reporting.  
   - **Visualization**: Power BI dashboards connected to Synapse.  

---

### **🛠️ Tools & Technologies**  
| **Category**       | **Tools Used**                                      |  
|---------------------|-----------------------------------------------------|  
| **Orchestration**   | Azure Data Factory (Dynamic Pipelines, Parameters)  |  
| **Transformation**  | Azure Databricks (PySpark, Spark SQL)               |  
| **Storage**         | Azure Data Lake Gen2 (Bronze/Silver/Gold containers)|  
| **Analytics**       | Azure Synapse Analytics (Dedicated SQL Pool)        |  
| **Visualization**   | Power BI                                            |  

---

### **🚀 Key Features**  
1. **Dynamic Data Ingestion**:  
   - ADF pipelines use **parameters and loops** to process 10+ tables from APIs dynamically.  
   - Example: Auto-fetching `Sales_2015.csv`, `Sales_2016.csv`, etc., without hardcoding paths.  

2. **PySpark Transformations**:  
   - **Data Cleaning**: Split product codes, handle nulls, parse dates.  
   - **Advanced Functions**: `withColumn`, `groupBy`, `concat_ws`, and window functions.  
   - **Data Analysis**: Aggregated sales trends and visualized results in Databricks notebooks.  

3. **Cost Optimization**:  
   - Used **locally redundant storage (LRS)** for non-critical data.  
   - Auto-terminating Databricks clusters to save costs.  

4. **Interview-Focused Scenarios**:  
   - Solved questions like *“Blob vs. Data Lake?”*, *“Explain ADF triggers”*, and *“Dynamic vs. Static Pipelines”*.  

---

### **📈 Steps to Build**  
1. **Set Up Azure Resources**:  
   - Created Resource Group, Data Lake, ADF, Databricks workspace, and Synapse Analytics.  

2. **Ingest Data with ADF**:  
   - Built pipelines to pull CSV files from GitHub APIs into Bronze layer.  
   - Used **linked services** and **parameterized datasets** for scalability.  

3. **Transform in Databricks**:  
   - Read Bronze data, applied transformations (e.g., `split` product IDs, `to_timestamp`).  
   - Wrote transformed data to Silver layer (Parquet).  

4. **Serve Data in Synapse**:  
   - Created SQL tables in Synapse for reporting.  
   - Joined fact/dimension tables (e.g., `Sales` ↔ `Products`).  

5. **Connect to Power BI**:  
   - Built dashboards to visualize sales trends, product performance, etc.  

---

### **📌 Outcomes**  
- **Technical Skills Proved**:  
  - Built a **scalable, low-code pipeline** with ADF.  
  - Mastered Spark for big data transformations.  
  - Designed a cloud data warehouse in Synapse.  

- **Interview Impact**:  
  - Discussed **real-time use cases** (e.g., handling incremental loads, cost optimization).  
  - Explained architecture tradeoffs (e.g., why Medallion over a single-layer lake?).  

---

**🔗 GitHub Repo Contents**:  
- `ADF Pipelines`: JSON templates for dynamic data ingestion.  
- `Databricks Notebooks`: PySpark code for transformations.  
- `Synapse SQL Scripts`: DDL/DML for tables and views.  
- `Power BI Reports`: Sample dashboards.  

---
