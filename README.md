# Bank Customer Churn Analysis & BI Pipeline

[![Python](https://img.shields.io/badge/Python-3776ab?logo=python&logoColor=white)](https://www.python.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ed?logo=docker&logoColor=white)](https://www.docker.com/)
[![Metabase](https://img.shields.io/badge/Metabase-509ee3?logo=metabase&logoColor=white)](https://www.metabase.com/)

**End-to-end ETL pipeline analyzing bank customer churn with Python, PostgreSQL, Docker, and Metabase.**

<img width="976" height="769" alt="image" src="https://github.com/user-attachments/assets/120c0e3d-564a-46bf-ab17-537ed988605f" />


## Project Overview

**Objective:** Analyzed bank customer data to understand why 20.4% of customers are leaving. Built complete ETL pipeline from Excel to interactive dashboard.

**Dataset:** 10,000 European bank customer records from Maven Analytics (Chris Bruehl)

**Pipeline Architecture**
   <img width="1600" height="343" alt="image" src="https://github.com/user-attachments/assets/68c65813-3ec9-44d5-9fa7-a2503ff5de12" />

**1. Excel:** Raw data source (10,000 records, 13 fields)
<br>**2. Python/Jupyter:** Data cleaning, EDA, and feature engineering
<br>**3. PostgreSQL:** Structured data storage with secure connections
<br>**4. Docker:** Containerized Metabase deployment
<br>**5. Metabase:** Interactive dashboard with KPIs and filters

## Project Phases

### 1. Data Preparation & Exploratory Data Analysis (Python)

**Data Cleaning:**
- Merged related data tables using pandas
- Removed duplicate records
- Standardized data types and currency formats
- Handled missing values with categorical labeling and median imputation
- Identified and treated outliers through statistical analysis
- Normalized categorical label variations

**Exploratory Analysis:**
- Compared numeric features (balance, age, credit score) by churn status
- Distribution analysis and outlier treatment
- Correlation analysis between features
- Examined relationships between demographic features and churn behavior

**Feature Engineering:**
- Removed identifier columns not suitable for modeling
- One-hot encoded categorical variables with `pd.getdummies()`
- Created derived feature: **balance-to-income ratio** for wealth assessment

**Technologies:** Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook



### 2. Database Integration (PostgreSQL)

- Created PostgreSQL database using DataGrip IDE
- Established secure connections using SQLAlchemy with environment variables
- Automated data transfer from pandas DataFrame to database table
- Implemented proper indexing for query performance

**Technologies:** PostgreSQL, SQLAlchemy, DataGrip, psycopg2



### 3. Business Intelligence Deployment (Docker & Metabase)

- Deployed Metabase as Docker container
- Connected Metabase to PostgreSQL database
- Leveraged Metabase's auto-exploration features for initial insights
- Built custom interactive dashboard with multiple visualizations

**Technologies:** Metabase, Docker, Docker Desktop



## Key Findings

Based on comprehensive analysis of 10,000 customer records, several critical patterns emerged:

### 1. High-Value Customer Attrition
- **Churned customers** maintained significantly higher average balances: **€91,100 vs €72,700**
- Bank is losing its most valuable customers
- Revenue impact: substantial loss of high-net-worth accounts

### 2. Wealth Concentration Risk
- Customers who left had **26% higher balance-to-income ratios** (1.31 vs 1.04)
- Suggests dissatisfaction among customers with larger deposits relative to their income
- Indicates potential service quality or satisfaction issues with wealthy segments

### 3. Overall Churn Rate
- **20.4% churn rate** (2,037 out of 10,000 customers)
- Represents significant revenue loss
- Critical metric for revenue forecasting and retention strategies

### 4. Geographic Variation
- Churn patterns differ across countries (France, Germany, Spain)
- Specific markets show higher risk
- Regional strategies needed for targeted interventions

### 5. Age Factor
- **Middle-aged customers (40-50 years)** show distinct churn patterns
- Age-specific retention programs recommended
- Different age groups respond differently to retention efforts

### 6. Gender Patterns
- **Female customers:** 25.1% churn rate
- **Male customers:** 16.5% churn rate
- **Female customers are 1.5x more likely to leave**
- Gender-based service improvements needed



## Data Metrics & Dashboard

**Key Metrics on Interactive Dashboard:**
- Total churned customers: 2,037 (20.4% churn rate)
- Churn distribution by demographics and geography
- Financial behavior comparison between customer segments
- Balance and income analysis by churn status
- Age and gender segmentation
- Geographic churn distribution



## Technologies & Tools

| Category | Technologies |
|----------|---------------|
| **Languages** | Python, SQL |
| **Libraries** | Pandas, NumPy, Matplotlib, Seaborn, SQLAlchemy, psycopg2 |
| **Database** | PostgreSQL |
| **Tools** | Jupyter Notebook, DataGrip, Docker Desktop, Metabase |


