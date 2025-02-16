# Medallion-Architecture-on-Stock-Data

## Medallion Architecture
<img width="1105" alt="med_arch" src="https://github.com/user-attachments/assets/deb1711c-eb98-4796-930d-fe25711ff619" />


Stock-related data* is generated every second from multiple sources, including users, the market, and stock exchanges. The **Bronze Layer** captures raw data, consisting of user transactions, market information, and stock and company registration details from the stock exchange.

After aggregation and cleaning, the **Silver Layer** contains structured and detailed data at a granular level, making it suitable for further processing.

In the **Gold Layer**, data is aggregated into daily, monthly, and yearly summaries, optimizing it for reporting, dashboards, and business intelligence applications.

**The data used in this project is artificially generated and does not represent real financial data. However, it is designed to closely mimic real-world scenarios, ensuring that stock prices fluctuate within a reasonable range over time.*
