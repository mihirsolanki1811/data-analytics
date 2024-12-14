# data-analytics
# PROJECT 1 Data Analytic Platform for Parking Tickets: Descriptive Analysis
<img width="1048" alt="Screenshot 2024-12-11 at 3 17 05 PM" src="https://github.com/user-attachments/assets/5dfae090-9c3c-42e0-b962-d37fbb6bcbad" />

## Overview  
This project demonstrates the implementation of a data analytic platform for Vancouver's parking ticket data using AWS services. The dataset, sourced from Vancouver City's open data library, contains records filtered to 471 entries for focused analysis. The goal is to understand patterns and trends in parking violations and inform city council and traffic department decisions. The data was ingested into AWS S3, where encryption, versioning, and access constraints ensured secure storage. AWS Glue DataBrew was employed for data profiling, cleaning, and preparation, resulting in a refined dataset ready for analysis.

## Data Cleaning and Pipeline Design 
Data cleaning involved addressing missing values, renaming columns, and preparing the data for analytics. A visual ETL pipeline was constructed using AWS Glue to compute the percentage of violations by bylaw. This included schema changes, aggregation, and derived columns to generate insights. Cleaned datasets were saved in CSV and Parquet formats, and results were stored back in S3 for further usage.

## Descriptive Analysis Insight 
Descriptive analysis revealed that 58.5% of violations occurred under bylaw 2849 (e.g., time limits, school zones), 41% under bylaw 2952 (metered parking), and 0.5% under bylaw 9978. These insights enable stakeholders to identify major infraction areas and plan targeted interventions, optimizing city parking management and compliance.



# PROJECT 2 Data Analytic Platform for Parking Tickets: Exploratory Analysis
<img width="1140" alt="gif2" src="https://github.com/user-attachments/assets/1f6b071f-c081-4074-821d-954a7025e10b">

## Project Overview
The exploratory analysis aimed to identify relationships between bylaw and section violations on specific streets in Vancouver. Using the same cleaned dataset from descriptive analysis, the project examined patterns of bylaw breaches and section violations across different locations. This analysis helps understand whether citizens frequently violate specific bylaws or a broader range of rules.

## Data Pipeline Design
The ETL pipeline utilized AWS Glue to compute distinct bylaw and section violations per street. Two datasets were derived from the clean dataset: one for bylaw violations and another for section violations. Tools like aggregate functions, schema changes, and outer joins were used to integrate these datasets, summarizing violation patterns for each street. The results were stored in S3 for further use.
<img width="1338" alt="gif-3" src="https://github.com/user-attachments/assets/ddfcf1e5-6948-44f3-9e1b-4de11c075fd9">
## Key Insights 
The analysis revealed that Hornby Street had violations under two bylaws and six sections, while West 8th Avenue saw violations under two bylaws and five sections. These insights can guide resource allocation, inform policy adjustments, and help promote compliance through community engagement and targeted awareness campaigns.

# Project 3 Policy 8000p, evaluation of financial aid for professional development
## Business Case
The current level of financial aid performance for professional development needs to be evaluated to ensure alignment with HR's growth and development objectives. Specifically, the analysis focuses on understanding the financial aid approval rate for professional development across different professional levels of University Canada West (UCW) candidates. This insight will help HR refine resource allocation and address potential gaps in professional development funding.
<img width="1228" alt="Screenshot 2024-12-11 at 1 02 09 AM" src="https://github.com/user-attachments/assets/8d5d4bbe-6477-437f-b35f-1d742cbd03b0">
## Data Analytics Case 
The key objective is to determine the Financial Aid Approval Rate across professional levels and departments. The metric used to measure this is:

Financial Aid Approval Rate (%) = (Approved Candidates / Total Candidates) × 100

Additionally, the study evaluates how much grant is approved per candidate from different departments to assess fairness and growth support across the organization.

## AWS Procedures and Results

### Data Ingestion

The raw dataset containing financial aid requests and approvals was ingested into AWS S3.
Data was secured with encryption, versioning, and access controls to ensure privacy.
Data Profiling and Cleaning

### AWS Glue DataVrew 
AWS Glue DataBrew was used for profiling the dataset, revealing completion rates and missing entries.
Missing values in key fields like department, approval status, and grant amount were addressed, and unnecessary columns were dropped.
ETL Pipeline for Metric Calculation

### S3: Cleaned dataset for processing
Schema Changes: Dropped irrelevant fields such as request timestamps and comments.
Aggregate Functions: Computed total and approved candidates for each professional level and department.
Derived Columns: Calculated the financial aid approval rate and average grant amount per candidate.
Join Operations: Combined departmental grant data with candidate-level data for cross-analysis.
Storage: Final results were saved in S3 in CSV and Parquet formats for visualization.
Results

## Financial Aid Approval Rate 
The overall approval rate was computed for different professional levels, revealing higher approval rates for senior-level staff compared to entry-level candidates.
Grant Amount per Candidate: Average grant distribution showed significant variation across departments, with the Research and Development team receiving the highest grants per candidate.

# Project 4 Predicting Shipping Delays with AWS SageMaker Canvas

# Project Overview
This project aims to predict expected shipping delays using AWS SageMaker Canvas, leveraging real-world data sourced from traffic internet systems. The data is ingested via a public subnet and securely stored in an AWS S3 bucket for further analysis. By building a machine learning model, the project seeks to improve supply chain efficiency and decision-making for shipping logistics.

# Dataset Details
The dataset contains critical information for shipping delay prediction:

X-Shipping Distance: Numeric values representing the distance covered along the X-axis.
Y-Shipping Distance: Numeric values representing the distance covered along the Y-axis.
Shipping Priority: Text labels categorizing shipment urgency (e.g., high, medium, low).
Shipping Origin: Text values indicating the origin location of shipments.
Product ID: Text values representing unique identifiers for shipped products.
Order ID: Text values representing unique order identifiers.
Expected Shipping Delays: Numeric values indicating actual delays in shipment delivery (target variable).

# Methodology
1) Data Ingestion

Traffic internet data is collected via a public subnet and saved to an AWS S3 bucket for centralized storage.
Security measures, including bucket versioning, encryption, and access controls, ensure data integrity and privacy.

2) Data Exploration and Preparation
SageMaker Canvas is used to explore and clean the dataset, addressing any missing or inconsistent values.
Feature engineering is applied to improve model performance (e.g., encoding shipping priority, normalizing distances).

3) Model Building with SageMaker Canvas
A predictive model is developed in SageMaker Canvas to estimate expected shipping delays based on the provided features.
The model leverages SageMaker's AutoML capabilities to automatically test and select the best-performing algorithm.

4) Result Storage and Access
Predictions are stored in AWS S3 in CSV and Parquet formats for easy access and downstream analysis.

# Results and Insights
The model accurately predicts expected shipping delays based on historical data.
Insights can be used to:
Optimize shipping routes to reduce delays.
Adjust shipping priorities dynamically based on traffic conditions.
Improve overall supply chain efficiency.














