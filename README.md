# Build an Incremental ETL Pipeline with AWS CDK  

## 📌 Overview  
This project demonstrates how to build a **serverless incremental ETL pipeline** using **AWS Cloud Development Kit (CDK)** for analyzing **cryptocurrency data**. The pipeline leverages multiple AWS services to extract data from the **Alpha Vantage API**, stream and transform it in real time, and load it into **DynamoDB** for further analytics using **Glue, Athena, Flink, and QuickSight**.  

The goal is to enable a scalable, cost-effective, and reusable architecture that supports real-time ingestion and analytics of cryptocurrency datasets.  

---

## 🚀 Architecture  
The pipeline consists of the following components:  

1. **Data Producer Lambda** – Fetches cryptocurrency exchange data from the **Alpha Vantage API** and pushes it into an **AWS Kinesis Stream**.  
2. **Kinesis Stream** – Acts as the ingestion layer for streaming data.  
3. **Data Consumer Lambda** – Consumes data from Kinesis, transforms it, and stores it in **DynamoDB**.  
4. **S3 Bucket** – Stores processed data for backup and further analytics.  
5. **Glue Jobs** – Perform ETL operations on data from DynamoDB and S3.  
6. **Athena** – Queries transformed data.  
7. **Apache Flink + Zeppelin** – Real-time analytics on the Kinesis stream.  
8. **QuickSight** – Visualization and dashboarding.  

---

## 📂 Dataset  
- **Source:** [Alpha Vantage API](https://www.alphavantage.co/documentation/)  
- **Data Types:** Cryptocurrency exchange rates, stock market time series, foreign exchange data, technical indicators, and more.  
- **Format:** JSON responses, transformed into DynamoDB/S3 tables.  

---

## 🛠️ Tech Stack  
- **Language:** Python  
- **AWS Services:**  
  - AWS Lambda  
  - Amazon Kinesis  
  - Amazon DynamoDB  
  - Amazon S3  
  - AWS Glue  
  - Amazon Athena  
  - Amazon QuickSight  
  - AWS Cloud9  
  - AWS CDK (Infrastructure as Code)  

---

## 📖 Key Learning Outcomes  
- Understanding **AWS CDK** and Infrastructure as Code (IaC).  
- Building serverless data pipelines with **Lambda, Kinesis, DynamoDB, and Glue**.  
- Performing real-time analytics with **Apache Flink + Zeppelin**.  
- Querying datasets with **Athena** and visualizing insights with **QuickSight**.  
- Best practices in **AWS account security, cost optimization, and scalability**.  

---

## ⚡ Setup & Deployment  

### Prerequisites  
- AWS Account  
- AWS CLI & CDK installed  
- Python 3.9+  
- Alpha Vantage API Key  

### Steps  
1. **Bootstrap CDK Environment**  
   ```bash
   npm install -g aws-cdk
   cdk bootstrap
   ```  

2. **Clone Repository into AWS Cloud9**  
   ```bash
   git clone git@github.com:username/repository.git
   cd repository
   ```  

3. **Install Dependencies**  
   ```bash
   pip install -r requirements.txt
   ```  

4. **Deploy Stacks**  
   ```bash
   cdk deploy --all
   ```  

5. **Run ETL Jobs with Glue**  
   - Create a Glue Crawler for DynamoDB.  
   - Define Glue ETL jobs for transformations.  
   - Query with Athena.  

---

## 📊 Use Cases  
- Real-time **cryptocurrency market monitoring**.  
- **Trading strategy development** with predictive analytics.  
- **Blockchain transaction analysis**.  
- **Risk assessment** of volatile crypto markets.  
- Extensible for **financial datasets** beyond crypto.  

---

## ✅ Summary  
- Built a **serverless incremental ETL pipeline** with AWS CDK.  
- Implemented **data ingestion (Lambda + Kinesis)**, **transformation (Glue + Lambda)**, and **storage (DynamoDB + S3)**.  
- Enabled **real-time analytics** with Flink/Zeppelin and **ad-hoc querying** with Athena.  
- Demonstrated **cost-optimized and scalable architecture** suitable for financial data processing.  

---

## 👤 Author  
**Abhishek Shinde**  
- Master’s in Applied Data Science, Syracuse University  
- Data Engineer | BI Analyst | Cloud Solutions Architect  
