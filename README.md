# # 🛒 ShopSmart - Sales & Inventory Analytics Project

> End-to-end data analysis of ShopSmart retail operations covering sales, inventory, customers, products & suppliers.

![Excel](https://img.shields.io/badge/Excel-PivotTable%20%26%20Dashboard-brightgreen)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Tools](https://img.shields.io/badge/Tools-Excel%20%7C%20Word%20%7C%20ER%20Diagram-blue)

## 📌 Project Overview
ShopSmart is a retail company with diverse product categories (Electronics, Beauty, Home, Groceries). This project was completed as part of the AnalystLab assessment to analyze:

- Low inventory risks
- Supplier concentration
- Inventory value distribution
- Business recommendations

The goal is to reduce stockout risk and optimize supplier and inventory management.

## 📁 Repository Structure-

## 🗂️ Database Schema (ER Diagram)

**Entities:**

**1. Customers**
- PK: Customer_ID
- Attributes: First_Name, Last_Name, Gender, Age, Email, Phone, City, State, Registration_Date, Customer_Segment

**2. Products**
- PK: Product_ID
- FK: Supplier_ID
- Attributes: Product_Name, Category, Price, Cost_Price

**3. Orders**
- PK: Order_ID
- FK: Customer_ID, Product_ID
- Attributes: Order_Date, Quantity, Total_Amount

**4. Inventory**
- PK: Inventory_ID
- FK: Product_ID
- Attributes: Stock_On_Hand, Inventory_Value, Stock_Status

**5. Suppliers**
- PK: Supplier_ID
- Attributes: Supplier_Name, Contact, Location

**Relationships:**
- Customers 1---M Orders
- Products 1---1 Inventory
- Suppliers 1---M Products
- Products 1---M Orders

## 📊 Key Analysis & Findings

### 1. Low Inventory Value (Pivot: Sorted by Sum of Inventory Value ASC)
Lowest 5 items at risk of stockout:
- Groceries Item 283 - ₦29,960
- Electronics Item 41 - ₦37,972
- Electronics Item 9 - ₦56,210
- Electronics Item 291 - ₦60,051
- Beauty Item 107 - ₦68,250

**Insight:** 10+ items below ₦77k, dominated by Groceries & Electronics.

### 2. Supplier Concentration
- Maximum products per supplier: **2**
- Top suppliers: Rosales PLC, Matthews and Sons, Smith PLC, Dyer LLC, Jones Group
- Most suppliers supply only 1 product = fragmented base.

### 3. High Value Concentration
- Beauty Item 355 - ₦255,904
- Electronics Item 146 - ₦208,656
- Electronics Item 34 - ₦205,590

Home, Beauty, Electronics hold >70% of inventory value.

## 💡 Business Recommendations (Part 9)

**1. Auto Reorder System:** Set threshold `<10 units or <₦70k value`. Immediately reorder Groceries 283, Electronics 41 & 9. Use formula: `=IF(Stock<10,"LOW","OK")`

**2. Supplier Consolidation:** Retain top 10 suppliers supplying 2 products. Negotiate 5-10% bulk discount with Rosales PLC & Williams Group to cut costs.

**3. Push High-Value Stock:** Bundle high-value Beauty + Home items and promote Electronics series 280-305 to increase turnover.

**Risk Identified:** Stockout and lost sales due to lack of low-stock monitoring.
**Opportunity:** Premium bundling of high-value stock to increase average order value.

## 🛠️ Tools & Skills Demonstrated
- Microsoft Excel: VLOOKUP, PivotTables, Sorting, Filtering, SUMIF
- Data Cleaning & Data Modeling
- ER Diagram Design
- Business Reporting & Dashboarding
- Insight Generation & Recommendation

## 📝 How to Run
1. Clone repo
2. Open `ShopSmart_Dashboard.xlsx`
3. Check PivotTables: `Low Inventory by Value`, `Products per Supplier`, `Inventory by Category`
4. Add Product_Name to inventory using: `=XLOOKUP(A2, products!A:A, products!B:B)`

## 👤 Author
**Erezitome Ginamre**
Data Analysis shopSmart AnalystLab
Lagos, Nigeria
https://www.linkedin.com/in/erezitome-ginamre-b46162434?utm_source=share_via&utm_content=profile&utm_medium=member_android | [erezitomeginamre@gmail.com]

## 📄 License
This project is for educational purposes - AnalystLab Assessment.