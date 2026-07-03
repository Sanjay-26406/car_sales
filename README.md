# 🚗 Car Sales Data Analysis

A data analysis project exploring car sales trends, pricing patterns, and brand performance using Python, SQL, and Power BI.

---

## 📌 Overview

This project analyzes a dataset of **468,000+ car sales records** to uncover meaningful insights about market trends, pricing factors, and regional sales distribution. The pipeline covers data cleaning, SQL-based exploration, and interactive dashboard visualization.

---

## 🎯 Objectives

- Analyze car sales data to identify key market trends
- Find top-performing car brands and models
- Understand price variations based on year, make, model, and mileage
- Visualize insights through an interactive Power BI dashboard

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python (pandas) | Data cleaning & preprocessing |
| SQL | Data analysis & querying |
| Power BI | Dashboard & visualization |
| Excel / Power Query | Additional data transformation |

---

## 📂 Dataset

| File | Description |
|------|------------|
| `data/raw_data.csv` | Original, unprocessed car sales data |
| `data/cleaned_data.csv` | Cleaned dataset (~468K records) |

**Columns in cleaned dataset:**

| Column | Type | Description |
|--------|------|-------------|
| `year` | int | Manufacturing year of the car |
| `make` | str | Car brand (e.g., BMW, Kia, Volvo) |
| `model` | str | Car model name |
| `sellingprice` | int | Final sale price (USD) |

---

## 🧹 Data Cleaning

Performed using **Python (pandas)**:

- Removed duplicate records
- Dropped rows with missing values
- Selected relevant columns (`year`, `make`, `model`, `sellingprice`)
- Standardized column names
- Converted data types (year → int, sellingprice → int)

```python
import pandas as pd

df = pd.read_csv("car_prices.csv")
df = df.drop_duplicates()
df = df.dropna()
df = df.iloc[:, [0, 1, 2, 14]]
df.columns = ["year", "make", "model", "sellingprice"]
df["year"] = df["year"].astype(int)
df["sellingprice"] = df["sellingprice"].astype(int)
```

---

## 💻 SQL Analysis

Key queries written in `sql/analysis.sql`:

- Total number of cars sold
- Average selling price overall and by brand
- Sales volume by state
- Top car brands and models by revenue
- Monthly sales trends over time
- Price comparison: MMR vs actual selling price

---

## 📊 Power BI Dashboard

The dashboard (`dashboard/project1.pbix`) includes:

- **Sales by State** — geographic distribution of sales
- **Monthly Sales Trend** — time-series view of volume and revenue
- **Top Car Brands** — ranked by units sold and average price
- **Price Distribution** — histogram of selling prices
- **Transmission Analysis** — breakdown by transmission type

---

## 💡 Key Insights

- Certain brands (e.g., BMW, Ford) consistently dominate by volume and revenue
- Sales vary significantly by state, with a few states accounting for the majority
- Lower-mileage vehicles command noticeably higher prices
- Seasonal patterns are visible in monthly sales trends

---

## 📁 Project Structure

```
Car-Sales-Analysis/
│
├── data/
│   ├── raw_data.csv
│   └── cleaned_data.csv
│
├── sql/
│   └── analysis.sql
│
├── dashboard/
│   └── project1.pbix
│
└── README.md
```

---

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/car-sales-analysis.git
   cd car-sales-analysis
   ```

2. **Install dependencies**
   ```bash
   pip install pandas
   ```

3. **Run data cleaning**
   ```bash
   python data_cleaning.py
   ```

4. **Run SQL analysis**  
   Import `data/cleaned_data.csv` into your SQL environment and run `sql/analysis.sql`

5. **Open the dashboard**  
   Open `dashboard/project1.pbix` in Power BI Desktop

---

## 📌 Conclusion

This project demonstrates a complete data analytics workflow — from raw data ingestion and Python-based cleaning, through SQL-driven analysis, to an interactive Power BI dashboard. The results reveal actionable insights into car pricing and sales performance across brands and regions.

---

## 🙌 Author

**Your Name**  
B.Tech IT Student | Aspiring Data Analyst  

[![GitHub](https://img.shields.io/badge/GitHub-your--username-black?logo=github)](https://github.com/your-username)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://linkedin.com/in/your-profile)
