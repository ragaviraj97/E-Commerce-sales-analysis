# 📊 E-Commerce Sales Analytics – Power BI Project(Interactive dashboard creation using power BI)

## 📌 Project Overview
This project is built on a structured **E-Commerce transactional data model** designed for advanced analytics using **Power BI**.  
The solution follows **data modeling best practices** by separating **Fact**, **Dimension**, and **Calendar** tables to enable accurate time intelligence, profitability tracking, discount analysis, and performance reporting.

The model supports **interactive dashboards**, **paginated reports**, and **PDF exports**, making it business-ready and scalable.
Dashboard Navigation & Report Links.

Dashboard Navigation 
This Power BI report is designed with multiple interactive pages for detailed analysis. Below are the
dashboard pages and their intended navigation links within the Power BI Service:
• Sales Analysis Dashboard: Provides overall KPIs, YTD sales, category-wise profit, monthly
sales trends, and top/bottom product performance.
## 🔗 Dashboard Navigation & Report Links

This Power BI report is designed with multiple interactive pages to support focused and efficient analysis.  
Each page is accessible through page navigation buttons and direct links in the Power BI Service.
### 📊 Sales Analysis Dashboard
Provides overall KPIs, Year-to-Date (YTD) sales, category-wise profit, monthly sales trends, and top/bottom product performance.  
### 💰 Discount & Revenue Page
Focuses on discount distribution, revenue impact, profit margins, and discount-based performance insights. 
### 🗺️ Map Visual Page
Displays geographical sales distribution by region, state, and city to identify high-performing and underperforming locations.  

These navigation links improve report usability, streamline navigation, and enable faster, data-driven decision-making within the Power BI ecosystem.


---

## 🧱 Data Model Architecture

### ⭐ Star Schema Design
- **Fact Table**: Sales Transactions  
- **Dimension Tables**: Customer, Product, Geography  
- **Date Table**: Calendar (created using DAX)  
- **Relationship Type**: One-to-Many (Dimensions → Fact)

This design improves:
- Query performance
- Measure accuracy
- Time-based calculations
- Report readability

---

## 1️⃣ Order & Customer Dimension Attributes

These attributes describe **who purchased**, **where the purchase occurred**, and **how products are categorized**.  
They are **categorical fields** used for slicing, filtering, and drill-down analysis.

| Attribute        | Description                                | Data Type     | Usage |
|------------------|--------------------------------------------|---------------|-------|
| Order ID         | Unique identifier for each order           | Whole Number  | Transaction key |
| Customer Name    | Name of the customer                       | Text          | Customer analysis |
| Region           | Sales region (North, South, East, West)    | Text          | Regional comparison |
| City             | Customer city                              | Text          | City-wise insights |
| Location         | Combined Region–City field                 | Text          | Simplified filtering |
| Category         | High-level product category                | Text          | Category KPIs |
| Sub Category     | Detailed product classification            | Text          | Product mix analysis |
| Products         | Category–Subcategory combination           | Text          | Drill-down reporting |
| Product Name     | Specific product sold                      | Text          | Product ranking |

🔹 **Purpose**
- Acts as **dimension tables** in the star schema  
- Used only for **grouping, filtering, and slicing**  
- **No mathematical calculations**

---

## 2️⃣ Sales Fact Table Attributes

These fields store **quantitative measures** and transactional details.  
They form the foundation for **revenue, profit, and margin analysis**.

| Attribute           | Description                         | Data Type       | Analytical Role |
|---------------------|-------------------------------------|-----------------|-----------------|
| Quantity            | Units sold per order                | Whole Number    | Volume analysis |
| Unit Price          | Price per unit                      | Decimal Number  | Base pricing |
| Discount (%)        | Discount applied                    | Decimal Number  | Pricing strategy |
| Sales               | Gross sales value                   | Decimal Number  | Revenue metric |
| Profit              | Net profit after cost               | Decimal Number  | Profit tracking |
| Revenue             | Final revenue after discount        | Decimal Number  | Financial KPIs |
| Profit Margin %     | Profit as % of revenue              | Percentage      | Margin evaluation |
| Payment Mode        | Payment method used                 | Text            | Payment behavior |
| Month Text          | Month name derived from date        | Text            | Time visuals |
| Discount Category   | Discount band classification        | Text            | Discount impact |

🔹 **Fact Table Usage**
- Numeric fields support **SUM, AVERAGE, YTD, YoY**
- Core driver for **KPIs and business insights**
- Categorical fields enhance **storytelling & segmentation**

---

## 3️⃣ Calendar (Date) Table – Time Intelligence

A **dedicated Calendar table** is created using **DAX** to enable advanced time-based analysis.

### 🧮 DAX Logic (Conceptual)
- Date Range: **2023 – 2026**
- Columns created using `ADDCOLUMNS()`

| Attribute      | Description                  | Data Type     | Usage |
|---------------|------------------------------|---------------|-------|
| Date          | Continuous date field        | Date          | Fact relationship |
| Year          | Calendar year                | Whole Number  | Year trends |
| Month Number  | Numeric month (1–12)         | Whole Number  | Sorting |
| Month Name    | Month text (Jan–Dec)         | Text          | Friendly visuals |
| Quarter       | Q1–Q4                        | Text          | Quarterly analysis |
| Year Month    | Combined year & month        | Text          | Time axis |
| Week Number   | Week of the year             | Whole Number  | Weekly trends |

🔹 **Why Calendar Table Is Critical**
- Enables **YTD, QTD, PYD, YoY** calculations  
- Avoids ambiguity in date filtering  
- Improves model accuracy and performance  

---

## 4️⃣ Measures & KPIs

Measures are created using **DAX** and evaluated at **query time**.

### 📈 Key KPIs
- Total Sales  
- Total Revenue  
- Total Profit  
- YTD Sales / Profit / Quantity  
- Previous Year to Date (PYD)  
- Product Rank YTD  
- Top 5 Products Flag  

These KPIs drive **executive-level insights** and **trend analysis**.

---

## 5️⃣ Best Practices Followed

✔ Star Schema Design  
✔ Proper Data Types for Accuracy  
✔ Separate Fact & Dimension Tables  
✔ Dedicated Calendar Table  
✔ Optimized DAX Measures  

---

## 📊 Report Readiness Summary

This data model is optimized for:
- Interactive Power BI Dashboards  
- Paginated Reports & PDF Exports  
- Time Series & Profitability Analysis  
- Business-ready KPIs & Insights  

The clear separation of **attributes (dimensions)** and **measures (facts)** ensures:
- Accuracy  
- Scalability  
- Professional reporting standards  

---

## 🛠️ Tools & Skills Used

- **Power BI**
  - DAX
  - KPI Cards
  - Cards Visuals
  - Slicers & Dropdowns
  - Buttons
  - Maps
  - Tooltips
  - Flow Charts
  - Pie Charts & Bar Charts
- **Data Modeling & Cleaning**
- **Sales, Profit & Margin Analysis**
- **Business Insight Generation**

---


 

