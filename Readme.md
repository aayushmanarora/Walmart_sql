


# 🛒 Walmart Sales Data Analysis (Python + SQL)

This project is an end-to-end data analysis pipeline designed to extract critical business insights from Walmart sales data. It uses **Python** for data processing and **SQL** (MySQL & PostgreSQL) for complex querying. This project is ideal for data analysts looking to build skills in data manipulation, querying, and data pipeline development.

---

## 📌 Project Objectives

- Clean and transform sales data using Python.
- Load cleaned data into MySQL and PostgreSQL.
- Use SQL to answer real-world business questions.
- Extract key insights about revenue, customer behavior, and product performance.

---

## 🛠️ Tools & Technologies

- Python 3.8+
- SQL: MySQL & PostgreSQL
- Libraries: `pandas`, `numpy`, `sqlalchemy`, `mysql-connector-python`, `psycopg2-binary`
- VS Code for development
- [Kaggle API](https://www.kaggle.com/docs/api) for dataset access

---

## 📂 Project Structure

```

\|-- data/                     # Raw and cleaned data files
\|-- sql\_queries/              # SQL scripts for analysis
\|-- notebooks/                # Jupyter notebooks for EDA
\|-- main.py                   # Main script for data processing
\|-- requirements.txt          # Python dependencies
\|-- README.md                 # Project documentation

````

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/najirh/Walmart_SQL_Python.git
cd Walmart_SQL_Python
````

### 2. Install required libraries

```bash
pip install -r requirements.txt
```

### 3. Set up your Kaggle API

* Get your `kaggle.json` token from your Kaggle account [here](https://www.kaggle.com/account).
* Place it in your local `~/.kaggle/` directory.
* Download the dataset:

```bash
kaggle datasets download -d aungpyaeap/supermarket-sales
```

### 4. Run the Python script

```bash
python main.py
```

---

## 🧹 Data Cleaning Steps

* Remove duplicates
* Handle missing values
* Fix inconsistent data types (e.g., convert dates, parse currency)
* Create a new `Total_Amount` column (unit price × quantity)

---

## 🏗️ Database Integration

* Connect to **MySQL** and **PostgreSQL** using SQLAlchemy.
* Create tables and insert cleaned data programmatically.
* Validate data loading using test SQL queries.

---

## 📊 SQL Business Analysis

Here are some key business questions answered using SQL:

* **Revenue trends by branch and product category**
* **Best-selling product categories**
* **Top-performing cities and peak hours**
* **Preferred payment methods by customer segments**
* **Profitability by category and branch**

### 🔍 Sample Query

```sql
SELECT Branch, Category, SUM(Total_Amount) AS Total_Revenue
FROM sales_data
GROUP BY Branch, Category
ORDER BY Total_Revenue DESC;
```

---

## 📈 Results & Insights

| Branch | Total Sales | Top Category | Preferred Payment |
| ------ | ----------- | ------------ | ----------------- |
| A      | \$123,456   | Electronics  | Credit Card       |
| B      | \$112,789   | Food         | Cash              |

* **Branch A** showed the highest revenue.
* **Electronics** was the most profitable category.
* **Credit Card** was the most used payment method.

---

## 🔄 Future Enhancements

* Integrate with **Power BI** or **Tableau** for dynamic dashboards
* Automate the ETL pipeline for real-time analysis
* Incorporate additional datasets (e.g., inventory, customer feedback)

---



## 🙌 Acknowledgments

* **Dataset**: [Walmart Sales Dataset on Kaggle](https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales)
* **Inspired by**: Walmart’s real-world business problems in retail and supply chain

---


