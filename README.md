# 🚀 End-to-End Data Migration using Azure

This project showcases a full data pipeline migrating data from an on-premise SQL Server to Azure Synapse via Azure Data Factory, Data Lake, and Databricks.

---

## 🧰 Tech Stack

* **Azure Data Factory** – Data ingestion & orchestration
* **Azure Key Vault** – Secure credentials
* **Azure Data Lake Gen2** – Data storage (Bronze/Silver/Gold)
* **Azure Databricks** – Data transformation (PySpark + Delta)
* **Azure Synapse Analytics** – Serverless SQL views for BI tools
* **SQL Server (SSMS)** – Source data

---

## 🗂️ Pipeline Overview

### 🔸 Ingestion (Bronze Layer)

* Lookup & ForEach in ADF fetches table metadata
* Data copied from on-prem SQL to Data Lake in Parquet format

### 🔹 Transformation (Silver & Gold Layers)

* Databricks notebooks mount storage and process data
* Bronze ➝ Silver (cleaning), Silver ➝ Gold (standardizing)

### 🟡 Loading to Synapse

* Views created in Synapse via stored procedures
* Data is ready for Power BI or other BI tools

---

## ⚙️ Setup Summary

1. Set up resources: ADF, Databricks, Key Vault, Synapse, Storage
2. Create integration runtime and link services
3. Build ADF pipeline with Lookup ➝ ForEach ➝ Copy
4. Run Databricks notebooks for transformation
5. Use Synapse to expose Gold data as SQL views
6. Schedule daily runs via triggers

---

## 💵 Cost Estimate (INR)

| Service     | Estimate  |
| ----------- | --------- |
| ADF         | ₹186.75   |
| Databricks  | ₹1,992.00 |
| Storage     | ₹8.30     |
| Synapse SQL | ₹8.30     |
| **Total**   | ₹2,195.35 |

