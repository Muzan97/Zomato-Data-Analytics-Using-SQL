# 🍽️ Zomato Data Analytics Project

## 📌 Project Overview

This project is a complete end-to-end data analysis case study on a Zomato-like food delivery platform. The work integrates Python for initial **exploratory data analysis**, SQL for **deep-dive business insights**, and a **relational database schema** to model the backend logic.

The analysis answers real-world questions a food delivery startup would care about — customer loyalty, rider performance, restaurant growth, revenue patterns, churn, and much more.

---

## 🎯 Business Objective

The core objective of this project is to use raw transactional data from a food delivery platform to drive actionable decisions by:

- Understanding **customer behavior** (retention, churn, loyalty)
- Analyzing **restaurant performance** across cities and time
- Evaluating **delivery metrics** such as average delivery time and success rate
- Tracking **order patterns** to optimize operations and promotions
- Identifying **high-performing riders** and **low-performing restaurants**
- Segmenting **customers** based on spend to tailor loyalty programs

---

## 🛠️ Database Schema (Snowflake Architecture)

The database follows a **snowflake schema** for efficient normalization, designed using SQL DDL statements and visualized via an ERD.

### 📦 Tables
- **orders** (fact table): stores transactions
- **customers**: user details and registration date
- **restaurants**: metadata like name, location, and hours
- **deliveries**: delivery details and status
- **riders**: rider information and sign-up time

![ERD](https://github.com/Muzan97/Zomato-Data-Analytics-Using-SQL/blob/main/Schema/ERD%20copy.jpg)

### 🧩 Relationships
```
orders (FACT)  
│  
├── customers (1:N)  
├── restaurants (1:N)  
├── deliveries (1:1)  
└── riders (1:N via deliveries)
```

Foreign keys and constraints were enforced to ensure data integrity.

✅ Files: `Snowflake_Schema.sql` and `ERD.jpg` inside the `schema/` folder.

---

## 🧪 Exploratory Data Analysis (Python)

Before building queries, I performed a detailed EDA in Python (Jupyter Notebook) using the `orders.csv` file:

- Checked for **nulls, duplicates, and inconsistencies**
- Verified **data types** and logical timestamp sequences
- Counted top **ordered dishes and high-value customers**
- Explored **temporal trends** (peak order hours, popular dates)
- Ensured quality before database import

✅ Notebook: `EDA_on_orders.ipynb` in the `python_eda/` folder.

---

## 🧠 SQL-Based Business Analysis

After schema setup and import, all in-depth business insights were derived using pure SQL. Over **15+ modules** of analysis were done using CTEs, window functions, aggregations, and conditional logic.

📁 File: `All_SQL_Queries_&_Insights.sql` inside the `sql_analysis/` folder

---

### 📚 Insight Modules Covered

| Module                            | Description |
|-----------------------------------|-------------|
| **Customer Retention**            | Loyal vs. Regular vs. Inactive users |
| **Customer Churn**                | Users who left after 2023 |
| **Revenue Analysis**              | By city, restaurant, and month |
| **Order Value & Volume**          | AOV per user, top spenders |
| **Time Slot Optimization**        | Peak and off-peak order hours |
| **Restaurant Growth Tracking**    | Monthly order growth ratio |
| **Rider Efficiency**              | Avg. delivery time, commission, and ratings |
| **Order Failures**                | Orders not delivered, riders/restaurants at fault |
| **Customer Segmentation**         | Based on total spend (Gold vs Silver users) |
| **Food Trends**                   | Top dishes by city and season |
| **Weekly Traffic**                | Top days of week for orders |
| **Cancellation Rate Trends**      | Comparison between 2023 and 2024 |

---

## 📊 Key Business KPIs Tracked

| 📌 Metric                        | 💡 Insight |
|----------------------------------|------------|
| **Customer Loyalty**             | 91.6% of active customers are highly loyal (5+ orders) |
| **Customer Churn**               | 9 out of 33 users did not return in 2024 |
| **Top Spend Customers**          | 14 users spent over ₹100,000 |
| **Average Order Value (AOV)**    | ₹310–₹340 for top users |
| **Delivery Failure Rate**        | 1 in every 12 orders failed |
| **Fastest Riders**               | 7 riders with consistent <15 min avg delivery |
| **Best Time to Order**           | Peak = 2 PM to 8 PM |
| **Most Ordered Dishes**          | Biryani, Masala Dosa, and Paneer Butter Masala |
| **Top Revenue City**             | Mumbai, followed by Bangalore & Delhi |
| **Restaurant Growth Leaders**    | Restaurant IDs 24, 12, 17, 34 with 50%+ monthly growth |

---

## 📁 Folder Structure

```
Zomato-Data-Analytics-Project/
├── README.md
├── schema/
│   ├── Snowflake_Schema.sql
│   └── ERD.jpg
├── python_eda/
│   └── EDA_on_orders.ipynb
├── sql_analysis/
│   └── All_SQL_Queries_&_Insights.sql
├── data/ (optional)
│   ├── orders.csv
│   ├── customers.csv
│   ├── restaurants.csv
│   ├── riders.csv
│   └── deliveries.csv
```

---

## 🔮 Future Enhancements

- 📊 Build interactive **Tableau/Power BI dashboards**
- 📅 Add **monthly cohort analysis** for retention trends
- 💬 Create a **recommendation engine** using item-pair logic
- 🌐 Host dashboard via Streamlit/PostgreSQL for live insights

---

## 🔗 Tools Used

- **SQL (PostgreSQL)** – for insights and data transformation  
- **Python (Pandas, NumPy)** – for initial EDA and preprocessing  
- **DB Schema Design** – Snowflake model  
- **ER Modeling** – Conceptualized via ERD  
- **Jupyter Notebook** – for EDA execution  

---

> 👨‍💻 Created with ❤️ by [Your Name] — Feel free to fork, use, or build on top of this.

