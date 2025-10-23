# E-commerce Sales Performance Dashboard

This Power BI project is a comprehensive analysis of the 100,000-order Brazilian E-commerce dataset from Olist. The objective was to build a multi-page dashboard to track key performance indicators (KPIs), analyze sales trends, and identify top-performing products and regions.

**View the live, interactive report here:** [Link to your published Power BI report]

---

## 🛠️ Tools & Technologies

- **BI Tool:** Power BI Desktop
- **ETL:** Power Query Editor
- **Data Modeling:** Star Schema (5 tables)
- **Language:** DAX (Data Analysis Expressions)
- **Key Concepts:** Time Intelligence, Data Cleaning, Report Navigation, Bookmarks

---

## ⚙️ Project Walkthrough

### 1. Data Cleaning and Transformation (ETL)
The raw dataset was loaded into the Power Query Editor for extensive cleaning and preparation.
- **Removed Duplicates:** Ensured data integrity by removing duplicate IDs from the `customers`, `orders`, and `products` tables.
- **Handled Date/Time Errors:** Solved complex text-to-date conversion errors by splitting the `order_purchase_timestamp` column, cleaning the data, and converting it to a pure `Date` type.
- **Filtered Bad Data:** Removed `(Blank)` and `(null)` values from key columns like `customer_state` to enable correct map visualization.

### 2. Data Modeling
A robust **Star Schema** was built in the Model View, which is the foundation of a professional BI report.
- **Fact Table:** `olist_order_items_dataset` (at the center).
- **Dimension Tables:** `olist_orders_dataset`, `olist_products_dataset`, `olist_customers_dataset`.
- **Date Table:** A dedicated `Dates` table was created using DAX (CALENDAR) to enable powerful time intelligence.
- **Relationships:** All tables were connected using the correct one-to-many (`1:*`) relationships.

### 3. Advanced DAX Measures
Authored complex DAX measures to calculate advanced KPIs, including:
- **Time Intelligence:** `Sales Previous Year`, `Orders Previous Year`, `Sales YoY %`, and `Orders YoY %`.
- **Latest Year KPIs:** Created "bulletproof" measures like `Sales YoY % (Latest Year)` that automatically show the most recent year's performance on KPI cards, solving the `(Blank)` context issue.
- **Key Business Metrics:** `Total Sales`, `Total Orders`, and `Average Sales per Order`.

### 4. Dashboard Design & Navigation
The final report is a multi-page, app-like experience.
- **Page 1 (Overview):** Features main KPIs, sales trends vs. the previous year, a Top 10 product category chart, and a filled map showing sales by state.
- **Page 2 (Product Details):** A "drill-down" page with a slicer to explore sales and order metrics for specific product categories.
- **Navigation:** **Buttons** and **Bookmarks** were implemented to allow seamless navigation between the "Overview" and "Product Details" pages.

---

## 📊 Final Dashboard Screenshots

*(Add your screenshots here)*

![Full Dashboard Overview](URL_to_your_screenshot_1.png)

![Product Details Page](URL_to_your_screenshot_2.png)