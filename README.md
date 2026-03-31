# 🛒 E-Commerce ETL Data Engineering Pipeline

## 📌 Project Overview

This project demonstrates a complete **end-to-end Data Engineering pipeline** built using Python, MySQL, Apache Airflow, and Power BI.

The goal is to simulate a real-world e-commerce system where raw data is transformed into clean, structured data and used to generate business insights through an interactive dashboard.

---

## 🚀 Project Architecture
- Raw Data (MySQL)
  - ↓
- Python ETL Pipeline
  - ↓
- Clean Data Warehouse (MySQL)
  - ↓
- Power BI Dashboard
  - ↓
-  Apache Airflow Automation


---

## 🧠 Key Features

- Automated ETL pipeline using Python
- Data cleaning and transformation
- Feature engineering (business metrics)
- Star schema data modeling
- Incremental data loading (no duplicates)
- Airflow DAG for automation
- Interactive Power BI dashboard
- Business-friendly data transformations

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|--------|
| Python (Pandas, SQLAlchemy) | ETL Processing |
| MySQL | Data Storage |
| Apache Airflow | Automation |
| Power BI | Data Visualization |
| Ubuntu (Linux) | Environment Setup |

---

## 📂 Dataset Details

The project uses multiple datasets:

- Customers
- Orders
- Order Items
- Payments
- Reviews
- Products
- Sellers
- Geolocation

---

## 🔄 ETL Pipeline Steps

### 🔹 1. Extract
- Data is extracted from MySQL raw database (`e_commerce_data`)

### 🔹 2. Transform
- Missing values handled
- Data types corrected
- Duplicates removed
- Feature engineering:
  - Delivery Days
  - Late Delivery Flag
  - Total Order Amount

### 🔹 3. Business Transformation
- State mapping (converted to Indian states)
- City standardization
- Product category transformation
- Payment type standardization

### 🔹 4. Load
- Clean data loaded into `e_commerce_clean_db`
- Fact and Dimension tables created:
  - `fact_orders`
  - `dim_customers`
  - `dim_products`
  - `dim_sellers`

---

## ⚡ Incremental Loading

- Only new records are inserted
- Prevents duplicate data
- Uses `order_id` for tracking

---

## ⏰ Airflow Automation

- DAG created using PythonOperator
- Scheduled to run daily
- Automates:
  - Data extraction
  - Transformation
  - Loading

---

## 📊 Power BI Dashboard


# 📊 Dashboard Preview

## 🧾 Main Dashboard
![Dashboard](https://github.com/Anshpatel1825/ecommerce-etl-data-engineering-pipeline/blob/main/Dashboard.png?raw=true)

---
### 🔹 Page 1: Executive Overview
- Total Revenue
- Total Orders
- Average Order Value
- Late Delivery %


## 👤 Customer Analysis
![Customer Analysis](https://github.com/Anshpatel1825/ecommerce-etl-data-engineering-pipeline/blob/main/Customer%20Analysis.png?raw=true)

---
### 🔹 Page 2: Sales Analysis
- Monthly Sales Trend
- Revenue by City
- Orders by State

## 🛒 Seller Analysis
![Seller Analysis](https://github.com/Anshpatel1825/ecommerce-etl-data-engineering-pipeline/blob/main/Saller%20Analysis.png?raw=true)
### 🔹 Page 3: Advanced Insights
- Review Distribution
- Seller Performance
- Late Delivery Trend

---

## 📈 Key Insights

- Maharashtra generates the highest revenue
- Credit Card is the most used payment method (~75%)
- Peak sales observed in May and July
- Late deliveries spike during certain months
- Top categories:
  - General Merchandise
  - Bedding & Bath
  - Beauty & Health

---

## 🧩 Data Model

Star Schema:

- Fact Table:
  - fact_orders

- Dimension Tables:
  - dim_customers
  - dim_products
  - dim_sellers

---

## 📌 Project Highlights

- Real-world ETL pipeline design
- Industry-level data modeling
- Automated workflow using Airflow
- Business-focused dashboard
- Clean and scalable architecture

---

## 📁 Project Structure
- ecommerce_etl_project/
- │
- ├── scripts/
- │ └── etl_pipeline.py
- │
- ├── dags/
- │ └── ecommerce_etl_dag.py
- │
- ├── data/
- │ └── raw_csv_files
- │
- ├── dashboards/
- │ └── powerbi_dashboard.pbix
- │
- └── README.md
