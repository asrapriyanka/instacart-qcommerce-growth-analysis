# 🛒 Instacart Q-Commerce Growth & Operational Analysis

An end-to-end data project simulating quick-commerce (Q-commerce) metrics, built to analyze customer retention drivers, hourly demand patterns, and unit economics using **Python, SQLite, and SQL**.

---

## 🚀 Project Overview
In quick-commerce models like Swish (10-minute delivery), understanding customer retention, dark store inventory workflows, and basket sizes is vital for unit economics. This project uses multi-table transactional datasets to extract high-impact product and operational insights.

* **Tech Stack:** Python, Google Colab, SQLite, Pandas, SQL
* **Dataset:** Instacart Market Basket Analysis (~130K+ orders)

---

## 📊 Key Findings & Insights

### 1. Retention Drivers (Category Reorder Rates)
* **Top Performers:** **Dairy/Eggs** (67.5% reorder rate) and **Produce** (66.46%) drive the highest repeat purchase frequency.
* **Business Takeaway:** These categories act as core habit-loop anchors. Quick-commerce platforms should use push notifications and personalized lifecycle messaging around weekly grocery replenishment cycles.

### 2. Operational Rhythm (Hourly Demand Curves)
* **Peak Window:** Order volume surges significantly starting at 8:00 AM (178K orders) and sustains a massive plateau between **10:00 AM and 4:00 PM** (averaging ~270K–288K orders per hour).
* **Business Takeaway:** Dark store inventory must be restocked *prior* to 8:00 AM during the low-volume overnight lull, and delivery rider shifts must be heavily staffed around the prolonged mid-day peak to maintain strict 10-minute SLAs.

### 3. Unit Economics (Basket Size & AOV)
* **Average Basket Size:** **10.55 items per order** (with a median of 9 items).
* **Business Takeaway:** Customers are utilizing the platform for substantial basket builds rather than single-item emergency orders, securing healthy Average Order Values (AOV) to offset fixed delivery costs.

---

## 💻 Technical Implementation
1. **Data Ingestion:** Loaded raw CSV files (`orders`, `products`, `departments`, `order_products`) into a relational local database (`instacart.db`) using Python and `sqlite3`.
2. **SQL Querying:** Wrote analytical queries leveraging multi-table `JOIN` operations, `GROUP BY` aggregations, and mathematical casting (`CAST`, `ROUND`) to evaluate category retention and hourly distributions.
