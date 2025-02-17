# Medallion-Architecture-on-Stock-Data

## Medallion Architecture
<img width="1105" alt="med_arch" src="https://github.com/user-attachments/assets/deb1711c-eb98-4796-930d-fe25711ff619" />


## Overview
This project is designed to process and analyze stock-related data generated every second from multiple sources, including user transactions, market information, and stock exchange data. The data is artificially generated to mimic real-world scenarios, ensuring that stock prices fluctuate within a reasonable range over time. The project is structured in a medallion archictecture into three main layers: Bronze, Silver, and Gold, each representing a different stage of data processing and refinement.

## Key Features
- **Data Ingestion**: Import data from MySQL and MongoDB databases using environment variables for secure connections.

- **Data Processing**: Clean, enrich, and structure raw data into meaningful formats.

- **Data Aggregation**: Aggregate data into hourly, daily, monthly, and quarterly summaries for comprehensive analysis.

- **Output Generation**: Generate CSV files containing aggregated data for further analysis and reporting.

- **CI/CD Testing**: Implement continuous integration and deployment (CI/CD) testing to ensure code quality and reliability.

## Data Layers
### Bronze Layer

The Bronze Layer captures raw data from various sources, including:

- User transactions

- Market information

- Stock and company registration details from stock exchanges

This layer stores the data in its most raw form, without any transformations or cleaning.

### Silver Layer

The Silver Layer processes the raw data from the Bronze Layer by:

- Cleaning and structuring the data

- Enriching it with additional details

- Aggregating it at a granular level for further processing

This layer ensures that the data is ready for more advanced analysis and reporting.

### Gold Layer

The Gold Layer further aggregates the data into daily, monthly, and yearly summaries, optimizing it for:

- Reporting

- Dashboards

- Business intelligence applications

This layer provides a high-level overview of the data, making it easier to derive insights and make informed decisions.

## Data Aggregation
The project aggregates stock-related data into four main timeframes:

1. Hourly

2. Daily

3. Monthly

4. Quarterly


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

