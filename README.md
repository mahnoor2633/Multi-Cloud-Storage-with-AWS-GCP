This project demonstrates how to build a multi-cloud storage backup pipeline by copying objects from AWS S3 into Google Cloud Storage (GCS) using Google Storage Transfer Service. The goal is to create a resilient, reliable, and vendor-lock-in–avoidant storage design for data availability and disaster recovery. 


**WHAT THIS PROJECT COVERS**

- Creating and populating an AWS S3 bucket (source). 

- Configuring a Storage Transfer Service job in GCP to move data from S3 → GCS. 

- Implementing federated identity access using an AWS IAM Role so GCP can access S3 using short-lived credentials (no long-term access keys). 

- Creating a GCS bucket (destination) and verifying the transfer results. 

**ARCHITECTURE (HIGH-LEVEL)**

- AWS S3 (source bucket) → GCP Storage Transfer Service → GCS bucket (destination)

- Federated access is handled via an AWS IAM role trusted by Google’s Storage Transfer identity. 

**PREREQUISITES**

- AWS account

- GCP account 

**STEP-BY-STEP IMPLEMENTATION**
https://docs.google.com/document/d/19zTzB8bZQMx0na-Jsyk5-mCGk7_uwIUBa0rw_Sq5XJk/edit?usp=sharing

**SECURITY NOTES**

- Uses federated identity instead of long-lived AWS keys.

- Access is granted via short-lived session credentials, reducing credential exposure risk.
