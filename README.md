# **Global Food Price Analysis 2025 (Professional Simulation)**
Our Team:
<img width="1238" height="692" alt="image" src="https://github.com/user-attachments/assets/e1bcdef2-35db-458a-bd29-b873b983f6df" />

Our Presentation: https://www.canva.com/design/DAG96YnXhx0/kbcujlqnlnHz0QogCEQ6KA/edit

Dashboard: https://public.tableau.com/views/CODA_RMT12_finalproj/Story1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

## **Project Overview**
This repository represents a **refined version** of my Capstone Project. While the initial iteration focused on direct analysis of flat datasets, this version simulates a **real-world enterprise workflow** where Data Analysts interact with a structured Data Warehouse prepared by Data Engineers.

Here, we simulate the transition from raw data to a **Star Schema** architecture, demonstrating my ability to work with relational data models and perform SQL-based analytics instead of simple flat-file filtering.

## **Problem Statement**
How can we analyze global food price dynamics in 2025 to identify price trends, market disparities, and economic correlations? The goal is to support operational decision-making (e.g., restocking strategies) and provide data-driven insights into purchasing power parity across different economic contexts.

---

## **The "Professional" Workflow**
Unlike typical beginner projects that load a single CSV, this project follows a strict **Data Modeling** approach:

### **1. Data Modeling (Star Schema)**
Instead of analyzing a monolithic dataset, we restructured the data into a **Fact Table** and **Dimension Tables** to optimize query performance and data integrity.

* **Fact Table**: `fact_food_price`
    * Contains transactional metrics: `price`, `usdprice`, and foreign keys to dimensions.
* **Dimension Tables**:
    * `dim_commodity`: Classification of items (`commodity_name`, `category`, `unit`).
    * `dim_country`: Country metadata including **GDP per Capita** (`country_name`, `iso3`, `gdp`).
    * `dim_market`: Geospatial data (`market_name`, `latitude`, `longitude`, `admin1`).

### **2. Simulated ETL Process**
* **Extract**: Ingested raw data from WFP (Food Prices) and World Bank (GDP).
* **Transform**: Used Python to split the "flat" raw data into relational tables, simulating the job of a Data Engineer.
* **Load**: Loaded these tables into a SQL-compatible environment for analysis.

---

## **Key Analytical Insights**
Using **SQL Joins** and statistical correlation, I derived the following insights:

1.  **Economic Correlation**: Found that a country's income level (GDP) is **not the primary driver** of food prices. Supply chain dynamics and market structure play a much larger role (Insight KQ7).
2.  **Currency Impact**: Countries with significant currency devaluation experienced local price spikes that decoupled from global USD trends (Insight KQ5).
3.  **Market Disparities**: Identified consistent "High-Cost" vs "Low-Cost" countries across specific commodities, providing a watchlist for potential supply shocks (Insight KQ4).

---

## **Technology Stack**
* **Language**: Python 
* **Data Modeling**: Star Schema Design (Fact/Dims).
* **Querying**: SQL (Simulated via Pandas/DuckDB).
* **Visualization**: Matplotlib, Seaborn, Tableau.

---

## **Repository Structure**
* `etl_simulation.ipynb`: The process of converting raw CSVs into Fact/Dimension tables.
* `analytical_queries.ipynb`: Performing analysis using SQL logic (Joins & Aggregations) on the structured data.
* `data/`: Contains the raw WFP data and the processed Dimension/Fact tables.

---

*“This project demonstrates my readiness to collaborate in a cross-functional data team, understanding not just how to analyze data, but how it should be structured for scalability.”*

