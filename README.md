# Medallion-Architecture-on-Stock-Data

## Medallion Architecture
<img width="1105" alt="med_arch" src="https://github.com/user-attachments/assets/deb1711c-eb98-4796-930d-fe25711ff619" />

## Project Overview

**StockMedallionPipeline** is a data engineering project demonstrating the implementation of **Medallion Architecture** for stock market data. The architecture organizes data into three layers — Bronze, Silver, and Gold — to efficiently capture, clean, transform, and analyze stock data.

This project processes stock data from multiple sources, including user transactions, market price updates, and stock exchange records, simulating a real-world financial data processing pipeline.

> ⚠️ **Note:** All data used in this project is artificially generated and does not represent real financial data. However, the data is designed to mimic realistic stock price fluctuations, transactions, and market behavior.

---

## Medallion Architecture

### Bronze Layer
- Raw ingestion layer
- Captures:
    - User transactions (from MongoDB)
    - Market and stock registration data (from MySQL)
- Data in its rawest form for traceability.

### Silver Layer
- Cleansed and enriched layer
- Structured, validated, and linked data
- Combines transaction data with stock and market data

### Gold Layer
- Aggregated layer for analytics and reporting
- Data summarized at:
    - **Hourly**
    - **Daily**
    - **Monthly**
    - **Quarterly**

---

## Key Features

- **Data Integration**
    - Load structured stock and market data into MySQL.
    - Load unstructured transactions data into MongoDB.
    - Extract data from MySQL and MongoDB into Spark for processing.
- **Medallion Processing Pipeline**
    - Transform Bronze data to Silver via validation, cleansing, and enrichment.
    - Aggregate Silver data to Gold at different time granularities (hourly, daily, monthly, quarterly).
- **Analytics Ready**
    - The Gold Layer data is structured for BI tools, dashboards, and further analytical exploration.
- **Pyspark-based Aggregation**
    - All data transformation and aggregation logic uses **PySpark** only.
    - No `pandas` or other Python data processing libraries are allowed.

---

## Tech Stack

- **Python 3.8+**
- **MySQL**
- **MongoDB**
- **Apache Spark (PySpark)**

---

## Dataset Description

- **Stock Market Data (`stock_market.sql`)**
    - Contains stock listings, market data, and price history.
    - Stored in MySQL.
- **User Transactions Data (`transactions.json`)**
    - Contains user buy/sell transactions with timestamps.
    - Stored in MongoDB.

---


## CI/CD Testing

To ensure the reliability and quality of the code, the project includes a CI/CD pipeline that performs the following tests:

1. **Format Check**: Ensures that the code adheres to the required formatting standards.

2. **Security Check**: Verifies that the code does not contain any security vulnerabilities.

3. **Protected Files Check**: Ensures that critical files are not modified or deleted.

4. **Data Validation**: Validates the integrity and accuracy of the processed data.

5. **Function Length Check**: Ensures that functions are concise and adhere to best practices.

## Project Structure

- `src/`
  - `data_processor.py`: Implementing the data processing methods
  - `main.py`: Main script orchestrating the data processing pipeline
- `data/`
  - `stock_market.sql`: MySQL database dump
  - `transactions.json`: MongoDB transaction data
- `.env.example`: Template for environment variables
- `config.yaml`: Configuration file for environment

## License and Usage Restrictions

Copyright © 2025 Zimeng Lyu. All rights reserved.
This project was developed by Zimeng Lyu for the RIT DSCI-644 course, originally designed for GitLab CI/CD integration. It is shared publicly for portfolio and learning purposes.

🚫 Usage Restriction:
This project may not be used as teaching material in any form (including lectures, assignments, or coursework) without explicit written permission from the author.

📩 For inquiries regarding usage permissions, please contact Zimeng Lyu at zimenglyu@mail.rit.edu.

