# Trade Statistics of India 📊🇮🇳

A Data Analytics project focused on creating a **clean, standardized, and large-scale dataset** of India’s import and export trade statistics using official government sources.

---

## 📌 Project Overview

India’s trade data is publicly available but highly **scattered, inconsistent, and difficult to analyze**. This project builds a **novel, structured dataset** by scraping and processing import–export data and enables meaningful analysis through visualization tools.

- **Course:** Data Analytics (CS61061)
- **Institute:** IIT Kharagpur
- **Dataset Size:** ~6 million filtered records
- **Time Period:** 2022 – 2024

---

## ❓ Problem Statement

- Trade data is spread across multiple HTML-based government portals  
- No standardized format for commodity, country, quantity, and time  
- Manual extraction is slow, error-prone, and not scalable  

**Goal:** Create a reliable, analytics-ready dataset for research, policy analysis, and business insights.

---

## 🎯 Objectives

- Collect and organize India’s import & export statistics
- Build a clean and consistent dataset
- Enable trade analysis and visualization
- Support economic research and decision-making

---

## 🛠 Tools & Technologies

### Languages & Libraries
- Python 3.11+
- BeautifulSoup4 (Web Scraping)
- Requests (Session handling & CSRF)
- Pandas (Data cleaning & transformation)

### Analytics & Visualization
- Power BI
- Tableau
- Jupyter Notebook

---

## 📂 Data Source

- Official Ministry of Commerce, Government of India  
  https://www.commerce.gov.in/trade-statistics/

---

## 🔄 Data Collection Methodology

1. Extract CSRF tokens from the portal
2. Iterate through all countries and months
3. Scrape commodity-wise import/export tables
4. Convert HTML tables into Pandas DataFrames
5. Merge records into a unified dataset
6. Export cleaned data in **CSV and JSON formats**

> Random delays and retries were used to ensure server-friendly scraping.

---

## 🧾 Dataset Schema

Each record contains:
- HS Code
- Commodity Name
- Month
- Year
- Country
- Unit
- Quantity
- Trade Type (Import / Export)

### Sample JSON
```json
{
  "Export": {
    "2022": [
      {
        "HS Code": "10063010",
        "Commodity Name": "Basmati Rice",
        "Month": "Jan",
        "Year": 2022,
        "Country": "United Arab Emirates",
        "Unit": "Tonnes",
        "Quantity": 14250
      }
    ]
  }
}
