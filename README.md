# 📊 Capstone Project: End-to-End Retail Data Pipeline  
### Using Python, SQL, PostgreSQL & Apache Airflow

---


## 🧠 Assignment Overview
**Duration:** 120 minutes  
**Submissions:** 42 student solutions  

This capstone project demonstrates how to build a **complete end-to-end data pipeline** that analyzes **daily sales revenue** from a PostgreSQL database and automates the workflow using **Apache Airflow**.

The project focuses on core **Data Engineering skills**, including data extraction, transformation, automation, and visualization.

---

## 🎯 Objective
Use **Apache Airflow** to automate a data pipeline that:
- Extracts sales data from PostgreSQL
- Calculates total daily revenue
- Visualizes revenue trends over time
- Runs as a scheduled DAG

---

## 🛠 Tools & Technologies
- **Python**
- **SQL**
- **PostgreSQL**
- **Apache Airflow**
- **Pandas & NumPy**
- **Matplotlib** (Data Visualization)

---

## 🔄 What the Pipeline Does

### 1️⃣ Extract
- Connects to **PostgreSQL**
- Extracts data from:
  - `orders`
  - `order_details`
- Saves the extracted data into a CSV file

---

### 2️⃣ Transform
- Loads the extracted CSV file
- Creates a new column `total_revenue` by:
  ```text
  total_revenue = quantity × price
  ```

* Groups data by sale_date
* Calculates **total revenue per day**
* Saves the transformed data to:

```
/home/kiwilytics/airflow_output/daily_sales_data.csv
```
---

### 3️⃣ Load & Visualize

* Reads daily_revenue.csv
* Converts sale_date to datetime format
* Plots **daily revenue as a time-series graph**
* Saves the output as:
```
/home/kiwilytics/airflow_output/daily_revenue_plot.png
```
---

### 🛫 Airflow DAG Workflow

The Airflow DAG automates the full pipeline with the following tasks:

#### 1. Extract Task
* Query PostgreSQL
* Export results to CSV
#### 2. Transform Task
* Read CSV
* Calculate total daily revenue
* Save results to a new CSV file

#### 3. Visualization Task
* Read aggregated data
* Generate and save a Matplotlib plot

Each task runs sequentially and is fully automated by Airflow.

---


### 📌 Assignment Question & Answer

> [!TIP]
> ❓ Question:
> After running your Airflow DAG, what is the total revenue on 1996-08-08?

> [!NOTE]
> ✅ Answer:
> Total Revenue on 1996-08-08 = 525.0

---

### 📈 Output Files

* daily_sales_data.csv
* daily_revenue.csv
* daily_revenue_plot.png

---

### 🧪 Key Skills Demonstrated

* SQL data extraction from PostgreSQL
* Data transformation using Pandas
* Aggregation and time-series analysis
* Workflow orchestration with Apache Airflow
* Automated data visualization
* End-to-end ETL pipeline design

---

### 🧠 Reflection: What I Learned

Through this exercise, I learned how to:

1. Use Apache Airflow to design and run a complete DAG
2. Extract data from multiple tables using SQL
3. Persist intermediate results using CSV files
4. Perform revenue calculations using Pandas
5. Aggregate transactional data by date
6. Visualize time-series data using Matplotlib

Build a reliable, automated data pipeline from start to finish

--- 

### 👤 Author

Moustafa Gaber

Data Engineering • Python • SQL • Airflow • ETL Pipelines
