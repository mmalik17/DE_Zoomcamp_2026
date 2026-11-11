# 🚕 NY Taxi Data Pipeline: Spark to BigQuery

An end-to-end batch data pipeline that ingests NYC taxi trip data, transforms it with Apache Spark, and loads it into Google BigQuery as a data warehouse for analysis.

> Personal project built as an extension of the Data Engineering Zoomcamp (Spark module), going beyond the scope of the homework.

---

## 📌 Project Overview

New York City's taxi system is one of the busiest urban transport networks in the world, and the NYC Taxi & Limousine Commission (TLC) publishes detailed trip records for it. Each record captures pickup and drop-off times and locations, trip distance, fare, tip, and payment type. For a transport operator, city planner, or ride-hailing business, this data helps answer questions such as when and where demand is highest, how fares and tips vary across zones and times of day, and how trip patterns change over time. 

In its raw form, though, the data is a large set of Parquet files that is hard to query and analyze. This project turns it into clean, structured tables in a data warehouse, so the business questions above can be answered with simple SQL queries and dashboards. The final result is a set of cleaned, analysis-ready data mart tables in Google BigQuery that can be queried directly for insights such as demand patterns, fare trends, and payment behavior.

**Goals**
- Ingest NYC taxi trip data from the public source into a Spark DataFrame
- Clean and transform the data using Spark SQL
- Load the transformed data into BigQuery for analytics and reporting

**Pipeline flow**

```
NYC TAXI WEB (source) ──► INGEST (Spark DataFrame) ──► TRANSFORM (Spark SQL) ──► LOAD (BigQuery DWH)
```

![Data Pipeline Spark Zoomcamp](https://github.com/user-attachments/assets/f177a474-bd38-43ae-bb07-f5b0962b8c09)

---

## 🏗️ Architecture and Tools Required

### Architecture

| Stage | Description |
|-------|-------------|
| **1. Source** | NYC TLC taxi trip data (Parquet files) downloaded from the official NYC Taxi website |
| **2. Ingest** | Data is read into a Spark DataFrame |
| **3. Transform** | Spark SQL is used for cleaning, type casting, filtering, and aggregation |
| **4. Load** | The final tables are written to Google BigQuery (data warehouse) |

### Tools & Technologies

The tools are listed in the same order as the pipeline flow: **Ingestion → Processing → Transformation → Data Mart → Load → Data Warehouse**.

| Data Tools | Role | Function |
|------------|------|----------|
| **PySpark** | Data Ingestion | Reads the raw trip data from the source into Spark. |
| **Apache Spark DataFrames** | Distributed Processing | Holds the ingested data in memory and processes it in parallel across the cluster. |
| **Spark SQL** | Transformation | SQL-based cleaning, type casting, filtering, and aggregation of the data. |
| **Data Mart Table** | Curated Output | Final transformed tables, ready for analytics and reporting. |
| **Google BigQuery** | Data Warehouse | Receives the data mart tables (data load) and serves them for analytical queries. |

### Prerequisites

- Python 3.9+
- Apache Spark and Java (JDK 11 or 17)
- A Google Cloud project with the BigQuery API enabled
- A GCP service account key (JSON) with BigQuery access
- Spark BigQuery connector

### How to Run

```bash
# 1. Clone the repository
git clone <your-repo-url>
cd <your-project-folder>

# 2. Install dependencies
pip install -r requirements.txt

# 3. Set your GCP credentials
export GOOGLE_APPLICATION_CREDENTIALS="path/to/your-service-account.json"

# 4. Run the pipeline
python <your_pipeline_script>.py
```

---

## 📂 Important Files

> Replace the file names below with the actual files in your project.

| File | Purpose |
|------|---------|
| `README.md` | Project documentation |
| `<pipeline_script>.py` | Main Spark job: ingest, transform, and load |
| `<notebook>.ipynb` | Exploratory analysis and step-by-step development |
| `requirements.txt` | Python dependencies |
| `images/` | Screenshots used in this documentation |

---

## ✅ Result

### Spark UI

The Spark UI was used to monitor jobs, stages, and execution performance while the pipeline ran.

<p align="left">
<img width="450" height="400" alt="Spark UI 1" src="https://github.com/user-attachments/assets/57a44188-6fc3-4d03-bb9a-04e3020821be" />
<img width="450" height="400" alt="Spark UI 2" src="https://github.com/user-attachments/assets/32dc4618-baa8-469f-baeb-593d021587fe" />
</p>

### Google BigQuery

The transformed data is loaded into BigQuery and is ready to be queried with standard SQL.

![BigQuery View](https://github.com/user-attachments/assets/64362ca6-139b-44a6-ae55-37dee49c45b2)

### Key Takeaways

- Built a working batch pipeline from a public web source to a cloud data warehouse
- Used Spark SQL for scalable transformation of large trip datasets
- Validated the job through the Spark UI and the final tables through BigQuery

### Future Improvements

- Orchestrate the pipeline with Airflow or Kestra
- Add data quality checks
- Build a dashboard (Looker Studio) on top of the BigQuery tables
