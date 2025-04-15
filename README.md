# Cloud Based Financial Analytics Pipeline for Bankruptcy Prediction

A cloud-native data pipeline built on AWS to centralize financial data, perform exploratory analysis, and predict bankruptcy risk using machine learning. This project demonstrates end-to-end integration of S3, Glue, Redshift, and SageMaker Canvas, enabling data-driven investment decisions for publicly traded companies.

- Presentation: [Cloud Pipeline Presentation]
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

## ML Model Results using AWS Sagemaker
![Visual Description](https://github.com/SalazarHerna/Cloud-Based-Financial-Analytics-Pipeline-for-Bankruptcy-Prediction/blob/9250191a90c58d3c74556cf677eccf3e35814084/CloudTechnology%20AWS/Sagemaker%20Model%20Results.jpeg)

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

#### Step 1: Data Lake – AWS S3
#### Step 2: ETL – AWS Glue
#### Step 3: Data Warehouse – AWS Redshift
#### Step 4: Machine Learning – AWS Sagemaker Canvas
