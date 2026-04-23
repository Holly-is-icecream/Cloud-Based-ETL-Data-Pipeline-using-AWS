# Cloud-Based ETL Data Pipeline using AWS

## 📌 Project Overview

This project demonstrates the design and implementation of a cloud-based ETL (Extract, Transform, Load) data pipeline using AWS services. The pipeline automates data ingestion, schema detection, data cleaning, and storage for downstream analytics.

The goal is to simulate a scalable data engineering workflow that processes raw data into clean, structured datasets.

---

## 🏗️ Architecture

```
Raw Data (CSV)
      ↓
Amazon S3 (Raw Layer)
      ↓
AWS Glue Crawler (Schema Detection)
      ↓
AWS Glue ETL Job (PySpark Transformations)
      ↓
Amazon S3 (Cleaned Layer)
      ↓
Amazon Athena (Query & Analysis)
```

---

## ⚙️ Tech Stack

* AWS S3 (Data Storage)
* AWS Glue (Crawler + ETL)
* PySpark (Data Processing)
* AWS Athena (Query Engine)

---

## 🔄 Data Pipeline Workflow

### 1. Data Ingestion

* Raw dataset is uploaded to Amazon S3
* Serves as the source for the ETL pipeline

### 2. Schema Detection

* AWS Glue Crawler automatically detects schema
* Metadata stored in Glue Data Catalog

### 3. Data Transformation (PySpark)

* Remove invalid or missing records
* Normalize inconsistent values (e.g., "NaN", empty strings)
* Convert data types (string → numeric)
* Handle missing values using statistical imputation (average)
* Round numeric values for consistency

### 4. Data Storage

* Cleaned dataset is written back to S3
* Organized into structured output for downstream use

### 5. Query & Analysis

* AWS Athena used to query cleaned dataset
* Enables scalable, serverless analytics

---

## 🚀 Key Features

* Automated schema detection using AWS Glue Crawler
* Scalable ETL pipeline using PySpark
* Data quality handling (missing values, normalization)
* Separation of raw and processed data layers
* Serverless architecture (no infrastructure management required)

---

## 📊 Example Transformations

* Removed rows with missing identifiers or names
* Standardized null values ("NaN", "", "null")
* Converted columns to numeric types
* Filled missing values using average imputation
* Rounded values to improve readability

---

## 📈 What I Learned

* Building end-to-end data pipelines in a cloud environment
* Using serverless AWS services for scalable data processing
* Applying data cleaning and transformation techniques
* Designing structured data workflows for analytics

---

## 🔧 Future Improvements

* Add automated scheduling (e.g., AWS Glue triggers)
* Implement data validation checks
* Integrate dashboarding tools (e.g., Tableau)
* Expand pipeline to handle streaming data

---

## 👤 Author

Holly Chen
