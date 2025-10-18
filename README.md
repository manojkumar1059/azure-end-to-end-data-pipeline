End-to-End Azure Data Engineering Pipeline

Technologies:

ADLS | Databricks | Azure SQL | Power BI | Azure Data Factory

Project Overview

This project demonstrates a complete data engineering workflow on Azure — from ingesting raw data to transforming, storing, and visualizing it.
The pipeline automates moving raw data from Azure Data Lake Storage (ADLS), processing it in Azure Databricks, loading it into Azure SQL Database, and creating interactive visualizations in Power BI.

Architecture & Components

Azure Data Lake Storage (ADLS): Stores raw and curated datasets.
Azure Data Factory (ADF): Orchestrates data pipelines using linked services and triggers.
Azure Databricks: Cleans, transforms, and aggregates data using PySpark.
Azure SQL Database: Stores the curated data for analysis.
Power BI Desktop: Connects to SQL Database for reporting and visualization.

Pipeline Flow

Get Metadata (ADF): Detects new files in ADLS.
Execute Notebook (ADF): Runs Databricks notebook for ETL processing.
Load Data (Databricks → SQL): Writes transformed data to Azure SQL Database.
Web Activity (ADF - Optional): Triggers Power BI dataset refresh (if using Power BI Service).
Power BI Desktop: Connects to SQL Database to visualize and refresh reports.

Dataset

Dataset Used: Sample Retail Sales Data
Source: Kaggle – Global Superstore Dataset
Columns:
Order_ID, Order_Date, Customer_Name, Region, Country, Category, Product_Name, Quantity, Unit_Price, Revenue, Profit

Technologies Used

Azure Data Lake Storage Gen2 (ADLS)
Azure Data Factory (ADF)
Azure Databricks (PySpark)
Azure SQL Database
Power BI Desktop
GitHub (Version control & documentation)

Key Insights

Electronics and Home & Furniture categories generate the highest revenue, while Clothing & Apparel and Accessories show moderate sales.
The West region contributes the largest share of total profit (≈29%), followed by South and Centre regions.
Total Revenue: 142.41M | Total Profit: 31.55M
South region shows strong performance across both revenue and profit metrics.
Revenue by State and Region visualization shows balanced sales coverage across major U.S. regions.
Time-series trend reveals noticeable revenue spikes around mid-2023 and early 2024, indicating peak sales periods.
Sub-category analysis highlights Small Electronics, Smartphones, and Wearables as top contributors by quantity sold.

Future Enhancements

Integrate Power BI Service for scheduled dataset refreshes
Implement Data Validation & Logging in ADF
Add CI/CD Integration using GitHub and Azure DevOps

