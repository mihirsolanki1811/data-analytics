# data-analytics
# PROJECT 1 Data Analytic Platform for Parking Tickets: Descriptive Analysis

# Project Overview <img width="1038" alt="git1" src="https://github.com/user-attachments/assets/542bce8a-0872-4470-bccd-b8b765289a8f">

This project demonstrates the implementation of a data analytic platform for Vancouver's parking ticket data using AWS services. The dataset, sourced from Vancouver City's open data library, contains records filtered to 471 entries for focused analysis. The goal is to understand patterns and trends in parking violations and inform city council and traffic department decisions. The data was ingested into AWS S3, where encryption, versioning, and access constraints ensured secure storage. AWS Glue DataBrew was employed for data profiling, cleaning, and preparation, resulting in a refined dataset ready for analysis.

# Data Cleaning and Pipeline Design
Data cleaning involved addressing missing values, renaming columns, and preparing the data for analytics. A visual ETL pipeline was constructed using AWS Glue to compute the percentage of violations by bylaw. This included schema changes, aggregation, and derived columns to generate insights. Cleaned datasets were saved in CSV and Parquet formats, and results were stored back in S3 for further usage.

# Descriptive Analysis Insight
Descriptive analysis revealed that 58.5% of violations occurred under bylaw 2849 (e.g., time limits, school zones), 41% under bylaw 2952 (metered parking), and 0.5% under bylaw 9978. These insights enable stakeholders to identify major infraction areas and plan targeted interventions, optimizing city parking management and compliance.



# PROJECT 2

# Data Analytic Platform for Parking Tickets: Exploratory Analysis
# Project Overview
The exploratory analysis aimed to identify relationships between bylaw and section violations on specific streets in Vancouver. Using the same cleaned dataset from descriptive analysis, the project examined patterns of bylaw breaches and section violations across different locations. This analysis helps understand whether citizens frequently violate specific bylaws or a broader range of rules.

# Data Pipeline Design
The ETL pipeline utilized AWS Glue to compute distinct bylaw and section violations per street. Two datasets were derived from the clean dataset: one for bylaw violations and another for section violations. Tools like aggregate functions, schema changes, and outer joins were used to integrate these datasets, summarizing violation patterns for each street. The results were stored in S3 for further use.

# Key Insights
The analysis revealed that Hornby Street had violations under two bylaws and six sections, while West 8th Avenue saw violations under two bylaws and five sections. These insights can guide resource allocation, inform policy adjustments, and help promote compliance through community engagement and targeted awareness campaigns.












