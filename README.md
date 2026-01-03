# Bank Customer Churn Analysis & BI Pipeline

[![Python](https://img.shields.io/badge/Python-3776ab?logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-f37726?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ed?logo=docker&logoColor=white)](https://www.docker.com/)
[![Metabase](https://img.shields.io/badge/Metabase-509ee3?logo=metabase&logoColor=white)](https://www.metabase.com/)

End-to-end ETL pipeline analyzing bank customer churn with Python, PostgreSQL, Docker, and Metabase.

**Excel** → **Python/Pandas** → **PostgreSQL** → **Docker/Metabase** → **Interactive Dashboard**

## Project Overview

This project analyzes 10,000 European bank customer records to identify churn patterns and risk factors. The pipeline transforms raw Excel data into an interactive dashboard.

<p align="center">
  <img width="800" alt="Bank Churn Analysis Dashboard - Metabase" src="https://github.com/user-attachments/assets/120c0e3d-564a-46bf-ab17-537ed988605f" />
</p>

**Dataset:** Bank Customer Data from [Maven Analytics](https://maven-datasets.s3.amazonaws.com/Bank+Customer+Churn/Bank+Customer+Churn.zip) (Chris Bruehl)

### Pipeline Architecture

The data flows through five stages: starting with raw Excel files, cleaned and analyzed in Python/Jupyter, stored in PostgreSQL database, deployed through Docker containers, and visualized in Metabase dashboard.

<p align="center">
  <img width="900" alt="Data Pipeline Flow" src="https://github.com/user-attachments/assets/68c65813-3ec9-44d5-9fa7-a2503ff5de12" />
</p>

## Project Phases

### 1. Data Preparation & Exploratory Data Analysis

**Data Cleaning:**
- Merged related data tables using pandas
- Removed duplicate records
- Standardized data types and currency formats
- Handled missing values with median imputation and categorical labeling
- Identified and treated outliers through statistical analysis

**Exploratory Analysis:**
- Compared balance, age, and credit score by churn status
- Distribution plots and correlation analysis
- Examined demographic features and churn behavior relationships

**Feature Engineering:**
- Removed identifier columns
- One-hot encoded categorical variables
- Created balance-to-income ratio for wealth assessment

**Technologies:** Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

### 2. Database Integration

- Created PostgreSQL database using DataGrip
- Established secure connections using SQLAlchemy with environment variables
- Automated data transfer from pandas DataFrame to PostgreSQL table

**Technologies:** PostgreSQL, SQLAlchemy, DataGrip, psycopg2

### 3. Business Intelligence Deployment

- Deployed Metabase as Docker container
- Connected Metabase to PostgreSQL database
- Built custom interactive dashboard with filters and visualizations

**Technologies:** Metabase, Docker

## Key Findings

### 1. High-Value Customer Attrition
Churned customers maintained significantly higher average balances: **€91,100 vs €72,700**, indicating the bank is losing its most valuable customers.

### 2. Wealth Concentration Risk
Customers who left had **26% higher balance-to-income ratios** (1.31 vs 1.04), suggesting dissatisfaction among customers with larger deposits relative to income.

### 3. Overall Churn Rate
**20.4% churn rate** (2,037 out of 10,000 customers) represents significant revenue loss.

### 4. Gender Disparity
- **Female customers:** 25.1% churn rate
- **Male customers:** 16.5% churn rate
- Females are **1.5x more likely to leave**

### 5. Age Factor
Middle-aged customers (40-50 years) show distinct churn patterns compared to other age groups.

### 6. Geographic Variation
Germany shows the highest churn rate at 32.4%, while France and Spain have lower rates at 16.2% and 16.7% respectively.

## Technologies

<table>
  <tr style="background-color: #f0f0f0;">
    <th>Category</th>
    <th>Tools</th>
  </tr>
  <tr>
    <td><strong>Languages</strong></td>
    <td>Python, SQL</td>
  </tr>
  <tr>
    <td><strong>Libraries</strong></td>
    <td>Pandas, NumPy, Matplotlib, Seaborn, SQLAlchemy, psycopg2</td>
  </tr>
  <tr>
    <td><strong>Database</strong></td>
    <td>PostgreSQL</td>
  </tr>
  <tr>
    <td><strong>Tools</strong></td>
    <td>Jupyter Notebook, DataGrip, Docker, Metabase</td>
  </tr>
</table>

## Project Highlights

- **End-to-End Pipeline:** Complete data flow from Excel to interactive visualization
- **ETL Automation:** Structured extraction, transformation, and loading workflow
- **Secure Connections:** SQLAlchemy with environment variables
- **Containerization:** Docker deployment with isolated environment setup
- **Data Quality:** Statistical outlier detection and treatment
- **Feature Engineering:** Created analytical features for deeper insights
- **Interactive BI:** Metabase dashboards with filtering capabilities

## Future Enhancements

- Develop machine learning model for churn probability prediction
- Implement automated data refresh pipeline for real-time updates
- Add Customer Lifetime Value (CLV) analysis
- Create customer segmentation using clustering algorithms
- Integrate additional data sources (transaction history, customer service interactions)

## Author

**Amirhossein Tonekaboni**  
SAP Business One Consultant | BI Developer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077b5?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tonekaboni/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white)](https://github.com/atonekaboni)
[![Portfolio](https://img.shields.io/badge/Portfolio-e53935?logo=google-chrome&logoColor=white)](https://atonekaboni.github.io)
