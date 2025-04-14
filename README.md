# Cloud Based Financial Analytics Pipeline for Bankruptcy Prediction

A cloud-native data pipeline built on AWS to centralize financial data, perform exploratory analysis, and predict bankruptcy risk using machine learning. This project demonstrates end-to-end integration of S3, Glue, Redshift, and SageMaker Canvas, enabling data-driven investment decisions for publicly traded companies.

---
## What Was Achieved?
Developed **cloud-native data architecture on AWS** for MSBA Financial Group that:

  1. Integrated decentralized data from three sources into a centralized Redshift data warehouse.
  2. Built a robust **ETL pipeline using AWS Glue** to create a “single source of truth.”
  3. Developed a **machine learning model using Amazon SageMaker Canvas** to predict bankruptcy risk.

**Key Business Outcome:**  
The model was used to evaluate 10 companies. Based on bankruptcy risk, investment was recommended for 3 companies with low-risk profiles.

## Data Flow Diagram
![Data Flow Diagram](https://github.com/SalazarHerna/Cloud-Based-Financial-Analytics-Pipeline-for-Bankruptcy-Prediction/blob/eb21ebb2e9ec799deb0f731da4410783004aef18/CloudTechnology%20AWS/DataFlow%20Diagram.jpeg)
---
## Insights

### Key Discoveries
- **Retained Earnings to Total Assets** | Was the most important predictor of bankruptcy (16.46% impact).
- **False positives** | Are less costly in this context and aligned with a conservative investment approach.
- **Data Integration** | Joining data sets (financials, ratios, and bankruptcy filings) led to a more robust, centralized data repository.
- **Automation Readiness** | Built the pipeline with future automation in mind, ensuring that the ETL process can be scaled easily when data ingestion volumes increase.

### Reflection
Cloud tools enabled efficient data transformation, scalable storage, and rapid model deployment. The architecture was designed with **future automation in mind**, using serverless and scalable AWS services.

## ML Model Results using AWS Sagemaker
![Visual Description](

---
## Project Description

The project was initiated to address the **CIO’s concern with decentralized data** across MSBA Financial Group. The data was originally stored across:

- `datacorp_financials.csv`: Vendor-provided income statements & balance sheets.
- `msba_fg_ratios.csv`: Analyst-calculated accounting ratios.
- `msba_fg_bankruptcy.csv`: Bankruptcy tracking by Analyst B.

Our goal was to **consolidate these sources, enable predictive modeling**, and help leadership make **informed investment decisions**.

---
## Tools Used

| Category              | Tools & Technologies Used                        |
|-----------------------|--------------------------------------------------|
| **Cloud Services**     | AWS S3, AWS Glue, AWS Redshift, AWS SageMaker Canvas |
| **ETL/Integration**    | AWS Glue, SQL                                   |
| **Modeling**           | AWS SageMaker Canvas                            |
| **Visualization**      | Confusion Matrix, AUC-ROC Curve (via Canvas UI) |
| **Presentation**       | PowerPoint (for the CIO Presentation)           |
| **Languages**          | SQL (Redshift)                                  |

## Steps towards building the Cloud Architecture

### Step 1: Data Lake – AWS S3
Created secure, scalable S3 Buckets to store raw data. This served as our **landing zone for all source files**.

### Step 2: ETL – AWS Glue
- Joined `datacorp_financials.csv` with `msba_fg_ratios.csv`.
- Cleaned and dropped redundant fields.
- Loaded into Redshift as `financials_combined`.
- Then joined `financials_combined` with `msba_fg_bankruptcy.csv` to create the final `training_set`.

### Step 3: Data Warehouse – AWS Redshift
- Created a Redshift Cluster: `msba-fingroup-cluster`
- Used Redshift Query Editor to:
  - Create tables: `financials_combined`, `bankruptcy`, `training_set`
  - Load and query integrated data

### Step 4: Machine Learning – AWS Sagemaker Canvas
- Used `training_set` to train a predictive ML model.
- Evaluated model metrics: **Accuracy: 93.475%, AUC-ROC: 0.922**
- Analyzed **feature importance** and **confusion matrix** to understand model behavior.
- Predicted bankruptcy risk for 10 new companies.
