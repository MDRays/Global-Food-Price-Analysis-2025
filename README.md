# **Global Food Price Analysis 2025 (Professional Simulation)**
Our Team:
<img width="1238" height="692" alt="image" src="https://github.com/user-attachments/assets/e1bcdef2-35db-458a-bd29-b873b983f6df" />

Our Presentation: https://www.canva.com/design/DAG96YnXhx0/kbcujlqnlnHz0QogCEQ6KA/edit

Dashboard: https://public.tableau.com/views/CODA_RMT12_finalproj/Story1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

## **Project Overview**
This repository represents a **refined version** of my Capstone Project. While the initial iteration focused on direct analysis of flat datasets, this version simulates a **real-world enterprise workflow** where Data Analysts interact with a structured Data Warehouse prepared by Data Engineers.

Here, we simulate the transition from raw data to a **Star Schema** architecture, demonstrating my ability to work with relational data models and perform SQL-based analytics instead of simple flat-file filtering.

## **Background**
In 2025, global food markets faced significant volatility due to shifting economic landscapes. This project analyzes the granular price data of essential commodities (Sugar, Salt, Potatoes, Onions, and Tomatoes) across 98 countries. By integrating World Food Programme (WFP) price data with World Bank GDP indicators, we aim to uncover the true correlation between a nation's wealth and its food security.

## **Problem Statement**
How do global food price dynamics in 2025 impact different economic strata? Specifically:
* Can we identify price trends and spikes across global markets?
* Does a higher GDP per capita guarantee more stable or lower food prices?
* How can data-driven insights optimize operational decisions, such as commodity restocking?.

---

## **Data Architecture & ETL Pipeline**
This project follows a professional Medallion Architecture approach to ensure data integrity:

### **1. Extract (Bronze Layer)**
* Data sourced from the WFP Humanitarian Data Portal.
* Multi-source integration: WFP Food Prices (CSV) + World Bank GDP (CSV).

### **2. Transform (Silver Layer - Star Schema)**
Using PySpark, we cleaned and modeled the data into a Star Schema for optimized querying:
* **Fact Table**: fact_food_price (Transactions, local prices, USD prices).
* **Dimension Tables**: dim_commodity, dim_country, dim_market, and dim_date.
* **Cleaning**: Removal of HXL Metadata tags and standardization of units (KG, Butir, etc.).

### **3. Load (Gold Layer)**
* Data is loaded into Neon PostgreSQL via Spark JDBC for final analysis and visualization.
---

## **Key Analytical Insights**
Based on the 7 Key Questions (KQ) addressed in the analysis phase:
* **1. Market Volatility** : Tomatoes and Onions exhibit the highest price variance, driven by seasonal local supply shifts.
* **2. The GDP Paradox** : High GDP per capita does not strictly correlate with lower food prices; local supply chains and stability are more dominant factors.
* **3. Currency Impact** : Countries facing local currency devaluation (detected via Price/USD ratio) suffer disproportionate food inflation.
* **4. Economic Outliers** : Countries like Yemen and Somalia show extreme price spikes (outliers) tied to accessibility and conflict issues.
* **5. Operational Efficiency** : Developed a logic to identify the cheapest markets per province to assist in cost-effective restocking strategies.

---

## **Technology Stack**
* **Language**: Python (Pandas, Seaborn, Matplotlib). 
* **Big Data Processing**: PySpark (ETL & Transformation).
* **Database**: Neon PostgreSQL (Data Warehousing).
* **Visualization**: Tableau.
* **Environment**: Docker & Jupyter Notebook.

---

## **Repository Structure**
* final_project_eda.ipynb: Data cleaning, unit standardization, and GDP merging.
* final_project_analysis.ipynb: Deep dive into the 7 Key Questions and economic correlations.
* cleaned_wfp_2025.csv: The processed dataset used for visualization.
* wfp_food_prices_global_2025.csv & GDP.csv: Raw data sources.
* airflow-with-spark.rar: Data Architecture & ETL pipeline
---

*“This project demonstrates my readiness to collaborate in a cross-functional data team, understanding not just how to analyze data, but how it should be structured for scalability.”*

