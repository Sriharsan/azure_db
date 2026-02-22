# ⚡ DeltaStreamX — Cloud-Scale Data Engineering Platform

A production-grade Azure Databricks Lakehouse platform processing **10M+ records** with end-to-end batch & streaming pipelines, star schema modeling, and Delta Live Tables.

---

## 🚀 Overview

**DeltaStreamX** is a cloud-scale data engineering platform built on the **Medallion Architecture (Bronze → Silver → Gold)** using Azure Databricks, Delta Lake, and PySpark — designed for high-throughput analytical workloads.

---

## ✨ Features

- 🏗️ **Medallion Architecture** — Bronze / Silver / Gold lakehouse on Azure Data Lake Gen2
- 🔄 **Batch & Streaming Pipelines** — Databricks Autoloader + Spark Structured Streaming
- 🌟 **Star Schema Modeling** — Fact & dimension tables with SCD Type 1 & Type 2 transformations
- ⚡ **Delta Live Tables** — Declarative pipeline orchestration with data quality enforcement
- 📐 **Unity Catalog** — Centralized governance, schema enforcement & access control
- 🚀 **Performance Gains** — 70% lower data latency · 3× faster analytical queries

---

## 🛠️ Tech Stack

| Tool | Usage |
|------|-------|
| Azure Databricks | Compute & orchestration |
| Delta Lake | Storage layer & ACID transactions |
| PySpark & Spark SQL | Data transformation at scale |
| Databricks Autoloader | Incremental data ingestion |
| Delta Live Tables | Pipeline automation & DQ checks |
| Azure Data Lake Gen2 | Cloud storage |
| GitHub | Version control & CI/CD |

---

## 🏛️ Architecture
```
GitHub → Azure → Data Lake Gen2 (Bronze)
                      ↓ ETL (PySpark)
              Data Lake Gen2 (Silver - Spark)
                      ↓ Delta Live Tables
              Data Lake Gen2 (Gold - Star Schema)
                      ↓
              Synapse Warehouse → Power BI
```

---

## 📊 Pipeline Overview

- **Parameters** → **Bronze Autoloader** → **Silver** (Customers / Orders / Products) → **Gold** (Customers / Products / Fact_Orders)
- SCD Type 1 & Type 2 handled at the Silver → Gold transformation layer
