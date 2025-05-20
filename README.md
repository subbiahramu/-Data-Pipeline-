
# 📊 **Serverless Data Pipeline for CSV Processing and Visualization**

This project automates the end-to-end processing and visualization of CSV files using AWS services like **S3**, **Lambda**, **Glue**, and **QuickSight**. The pipeline efficiently handles data ingestion, transformation, and real-time analytics to generate interactive dashboards for actionable insights.

## 🌟 **Project Overview**

This serverless data pipeline enables users to upload CSV files to **Amazon S3**, which triggers an **AWS Lambda** function to preprocess and clean the data. The data is then passed to **AWS Glue** for transformation and further ETL operations. Finally, **Amazon QuickSight** is used to create dynamic and interactive dashboards for visualizing the processed data.

---

## 🛠️ **Technologies Used**

* **Amazon S3**: Storage for raw, processed, and final CSV data.
* **AWS Lambda**: Preprocesses CSV data automatically on upload.
* **AWS Glue**: ETL (Extract, Transform, Load) service for data transformation.
* **Amazon QuickSight**: Visualization tool for creating dashboards and reports.
* **IAM Roles & Policies**: Secure access control for the services.

---

## 🚀 **Pipeline Workflow**

1. **Data Ingestion**

   * Users upload CSV files to an S3 bucket (e.g., `csv-raw-data`).

2. **Preprocessing with Lambda**

   * An **AWS Lambda** function is triggered by the S3 event to clean and preprocess the data (e.g., filter, format).

3. **ETL with AWS Glue**

   * **AWS Glue** performs detailed transformations on the preprocessed data and stores it in a structured format in the S3 `csv-final-data` bucket.

4. **Data Visualization with QuickSight**

   * **Amazon QuickSight** is connected to the final data and used to generate dynamic, interactive dashboards for reporting and analytics.

---

## 🔧 **Setup & Configuration**

### 1. **S3 Buckets**

* Create three S3 buckets:

  * `csv-raw-data` (for raw CSV uploads)
  * `csv-processed-data` (for preprocessed data)
  * `csv-final-data` (for transformed data)

### 2. **AWS Lambda Function**

* Write a Lambda function to preprocess data upon upload to the S3 raw data bucket.
* The function should filter and format the data before passing it to AWS Glue.

### 3. **AWS Glue Configuration**

* Set up **AWS Glue Jobs** for ETL processes: extract, transform, and load the preprocessed data into the final S3 bucket.
* Create a **Glue Data Catalog** and crawler for structured data.

### 4. **Amazon QuickSight**

* Set up **Amazon QuickSight** and create data sources connected to the processed S3 data.
* Create interactive dashboards for real-time data visualization.

---

## 📈 **Data Visualization Example**

Include screenshots of your **Amazon QuickSight dashboards** that show how the processed data is visualized, such as sales trends, customer data, or financial insights.

---

## ⚙️ **Estimated Time & Cost**

* **Time**: Approximately 3-4 hours for full setup and deployment.
* **Cost**: \~\$0.50 - \$1, depending on usage (AWS Free Tier eligible).

---

## 🧹 **Clean Up**

To avoid unnecessary charges, clean up the resources after use:

1. **Delete Amazon QuickSight Resources**

   * Remove dashboards, datasets, and analyses created in QuickSight.

2. **Delete S3 Buckets**

   * Empty and delete the S3 buckets (`csv-raw-data`, `csv-processed-data`, `csv-final-data`).

3. **Delete AWS Glue Resources**

   * Remove Glue Jobs, Data Catalog tables, and crawlers.

4. **Delete Lambda Functions**

   * Delete the Lambda function used for preprocessing.

5. **Remove IAM Roles & Policies**

   * Delete IAM roles associated with Lambda, Glue, and QuickSight.

---

## 📝 **Future Enhancements**

* Implement **batch processing** for handling large CSV files.
* Add **data validation** to ensure the integrity of processed data.
* Enhance **QuickSight dashboards** with more advanced visualizations.
* Integrate additional data sources for richer analytics.

---

## 📂 **Project Structure**

```
/serverless-csv-pipeline
│
├── /lambda
│   └── lambda_function.py       # Preprocessing script for CSV files
│
├── /glue
│   └── glue_job.py             # AWS Glue ETL job script
│
└── /quicksight
    └── dashboard_template.json  # QuickSight dashboard setup
```

---

