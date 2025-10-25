Got it! Here’s a **fuller, portfolio-ready README** for your GitHub, keeping all your details, workflow, key points, and personalization for **Youssef Bouzine**, while still being professional and visually appealing:

---

# 🏦 Top 10 Global Banks ETL Pipeline

This project implements a **complete Python ETL (Extract, Transform, Load) pipeline** developed by **Youssef Bouzine** to collect, process, and store market capitalization data for the top 10 largest banks in the world. The pipeline extracts data from Wikipedia, converts USD values into **GBP, EUR, and INR**, and stores it in both **CSV and SQLite database formats**, making it ready for analysis and reporting. Every stage of the process is logged with timestamps for monitoring and debugging.

---

## 📊 Project Overview

The ETL pipeline automates:

1. **Extraction** – Scrapes the top 10 banks and their market capitalization (USD) from Wikipedia.
2. **Transformation** – Converts USD to **GBP, EUR, and INR**, rounding to 2 decimals.
3. **Loading** – Saves the processed data into:

   * **CSV file** for portability
   * **SQLite database** for querying and analysis
4. **Logging** – Tracks each step with timestamped messages for traceability.

---

## 🎯 Goals

* Automate collection of global bank data.
* Enable multi-currency reporting for financial analysis.
* Store data in structured formats for analysis and distribution.
* Maintain clear logs to monitor pipeline execution.

---

## 🛠 Technologies Used

* **Python 3.x**
* **pandas** – Data manipulation and analysis
* **BeautifulSoup4** – HTML web scraping
* **requests** – HTTP requests
* **NumPy** – Numerical calculations
* **SQLite3** – Database management

---

## 📁 Project Structure

```
TOP10-GLOBAL-BANKS-ETL/
├── banks_pipeline.py        # Main ETL script
├── exchange_rate.csv        # Currency exchange data
├── Largest_banks_data.csv   # Output CSV
├── Banks.db                 # SQLite database
├── code_log.txt             # Execution log
└── README.md                # Project documentation
```

---

## 🔄 ETL Workflow

### **1. Extract**

* Scrapes Wikipedia to extract bank names and market capitalization in USD.
* Returns a **DataFrame** with columns `['Name', 'MC_USD_Billion']`.

### **2. Transform**

* Reads exchange rates from CSV.
* Converts USD to **GBP, EUR, INR**, rounding values to 2 decimals.
* Adds new columns: `MC_GBP_Billion`, `MC_EUR_Billion`, `MC_INR_Billion`.

### **3. Load**

* Saves the transformed DataFrame to a **CSV file**.
* Loads the data into **SQLite database** for querying.

### **4. Query & Analysis**

* Pre-configured SQL queries allow:

  * Viewing all bank data: `SELECT * FROM Largest_banks;`
  * Calculating average market cap in GBP: `SELECT AVG(MC_GBP_Billion) FROM Largest_banks;`
  * Listing top 5 banks: `SELECT Name FROM Largest_banks LIMIT 5;`

---

## 📝 Sample Output

| Name            | MC_USD_Billion | MC_GBP_Billion | MC_EUR_Billion | MC_INR_Billion |
| --------------- | -------------- | -------------- | -------------- | -------------- |
| JPMorgan Chase  | 432.92         | 346.34         | 402.62         | 35910.71       |
| Bank of America | 231.52         | 185.22         | 215.31         | 19204.58       |
| …               | …              | …              | …              | …              |

---

## 🔍 Key Features

* **Automated Web Scraping** – Extracts live data without manual input.
* **Multi-Currency Support** – Converts USD to GBP, EUR, INR.
* **Dual Storage** – CSV for portability, SQLite for database queries.
* **Execution Logging** – Logs each ETL step with timestamps.
* **SQL Query Ready** – Built-in queries for analysis and insights.

---

## 📚 Learning Outcomes

* Building **production-ready ETL pipelines**.
* Extracting structured data from **HTML web pages**.
* Transforming and manipulating financial data across multiple currencies.
* Storing and querying data using **SQLite**.
* Implementing logging and monitoring for ETL processes.

---

## 🚀 How to Run

### Prerequisites

```bash
pip install pandas beautifulsoup4 requests numpy
```

### Execution

```bash
python banks_pipeline.py
```

**Expected Outputs:**

* **Console** – Step-by-step logs and query results.
* **CSV File** – `Largest_banks_data.csv` with multi-currency market caps.
* **Database** – `Banks.db` with table `Largest_banks`.
* **Log** – `code_log.txt` with timestamped execution entries.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! This project is **open-source under MIT License**.

---

## 👤 Author

**Youssef Bouzine**
GitHub: [@youssefbouzine](https://github.com/youssefbouzine)
LinkedIn: Connect via LinkedIn

---

If you want, I can **also add emojis and color-coded headings** to make it even more **GitHub-portfolio-friendly**, while keeping it professional and visually engaging.

Do you want me to do that?
