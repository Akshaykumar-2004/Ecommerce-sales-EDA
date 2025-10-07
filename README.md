# 🛒 E-Commerce Sales Analysis

## 📌 Project Overview  
This project performs **Exploratory Data Analysis (EDA)** on an e-commerce retail dataset to uncover **sales trends, customer purchasing behavior, and revenue insights**.  
The analysis includes **data cleaning, feature engineering, outlier detection using the IQR method, and RFM (Recency, Frequency, Monetary) segmentation** to identify high-value customers.

The goal is to transform messy transactional data into **actionable insights** that support business decisions such as customer retention, pricing strategy, and inventory planning.

---

## 🧠 Objectives  
- Clean and prepare raw sales data for accurate analysis  
- Engineer key features like `TotalPrice`, `Year`, `Month`, and `DayOfWeek`  
- Detect and remove extreme values using the **Interquartile Range (IQR)** method  
- Segment customers using **RFM Analysis** to identify loyal and high-value buyers  
- Provide interpretable insights suitable for dashboarding and reporting  

---

## 🧰 Tech Stack  
**Language:** Python  
**Libraries:** pandas, numpy, matplotlib, seaborn  
**Dataset:** `online_retail.xlsx` (UCI Online Retail Dataset)

---

## ⚙️ Workflow  

### 1. Data Cleaning  
- Removed rows with missing `CustomerID`  
- Filtered out returns (`Quantity < 0`) and zero-priced items (`UnitPrice = 0`)  
- Converted `CustomerID` to integer type for consistency  

### 2. Feature Engineering  
- Created `TotalPrice = Quantity × UnitPrice`  
- Extracted date parts: `Year`, `Month`, `DayOfWeek`, `Hour` from `InvoiceDate`  
- Prepared dataset for time-based and behavioral analysis  

### 3. Outlier Detection (IQR Method)  
Applied statistical fences:  
Q1 = 25th percentile
Q3 = 75th percentile
IQR = Q3 - Q1
Lower Bound = Q1 - 1.5 * IQR
Upper Bound = Q3 + 1.5 * IQR
Filtered out transactions beyond these bounds to ensure robust averages.

### 4. RFM Analysis  
Computed customer metrics:  
- **Recency:** Days since last purchase  
- **Frequency:** Number of unique invoices  
- **Monetary Value:** Total amount spent  

Used these to rank customers and identify VIP segments.

---

## 📊 Key Insights  
- Majority of sales concentrated in specific months and weekdays (potential for promotional targeting)  
- High-frequency customers contribute disproportionately to total revenue  
- Outlier detection improved the reliability of average sales metrics  
- RFM segmentation revealed distinct loyalty tiers for customer retention programs  

---

## 🧾 Business Impact  
This analysis provides a foundation for:  
- **Customer segmentation** and loyalty marketing  
- **Revenue forecasting** and sales optimization  
- **KPI dashboards** in BI tools such as Power BI or Tableau  

---

## 🚀 Future Enhancements  
- Build a **Power BI dashboard** to visualize monthly sales and RFM segments  
- Integrate **SQL backend** for automated data refresh  
- Apply **K-Means clustering** for advanced customer segmentation  

---


