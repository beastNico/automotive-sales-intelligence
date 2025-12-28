# 🚗 Automotive Sales Intelligence Dashboard

An end-to-end **Power BI analytics dashboard** for analyzing automotive sales performance.  
Built on **23,906 transaction records**, this solution delivers actionable insights into sales trends, dealer performance, and market dynamics using advanced DAX time intelligence.

---

## 📊 Project Overview

This dashboard enables stakeholders to monitor sales performance across **time, geography, dealers, and vehicle attributes**, supporting data-driven decisions for pricing, inventory, and marketing.

**Key Highlights**
- Interactive executive dashboard with KPIs
- YTD, MTD, and YoY performance analysis
- Dealer and regional performance tracking
- Drill-through to transaction-level details
- Optimized star schema data model

---

## 🧭 Dashboard Pages

### 1️⃣ Overview Page (Executive Summary)

Provides a high-level snapshot of sales performance.

#### 🔹 KPI Cards
- **YTD Total Sales** (with MTD comparison)
- **YTD Average Sales Price** (variance indicators)
- **YTD Cars Sold** (growth metrics)

#### 🔹 Visualizations
- Weekly sales trend (line chart)
- Sales distribution by **Body Style** (donut chart)
- Sales distribution by **Color** (donut chart)
- Dealer performance **geographic heat map**
- Company-wise performance table

---

### 2️⃣ Details Page (Transaction Analysis)

Enables deep-dive analysis with flexible filtering.

#### 🔹 Filters
- Body Style  
- Dealer Name  
- Transmission Type  
- Engine Type  

#### 🔹 Data Grid
- Complete transaction-level data
- Sortable and filterable across all dimensions

---

## 🧠 Key Metrics & KPIs

### Core Measures
- **Total Sales**
- **Average Price**
- **Cars Sold**

### Time Intelligence
- **YTD / MTD / PYTD Sales**
- **YTD / MTD Avg Price**
- **YTD / MTD Cars Sold**

### Growth & Comparison
- YoY Sales Growth
- YoY Avg Price Growth
- YoY Cars Sold Growth
- Period-over-period variance
- Conditional KPI color indicators

---

## 🏗️ Data Architecture

### Dataset
- **Source**: Excel (.xlsx)
- **Total Records**: 23,906
- **Date Range**: 2022 (Full Year)
- **Primary Table**: `car_data`

### Data Model
- Star schema design
- One-to-many relationship:
```

Calendar[Date] → car_data[Date]

```
- Calendar table marked as Date Table for time intelligence

---

## 🧾 Data Dictionary

### `car_data` Table

| Field | Type | Description |
|------|------|-------------|
| Car_id | Text | Unique transaction ID |
| Date | Date | Sale date |
| Customer Name | Text | Customer identifier |
| Gender | Text | Customer gender |
| Annual Income | Number | Annual income |
| Dealer_Name | Text | Dealership name |
| Dealer_No | Text | Dealer code |
| Dealer_Region | Text | Geographic region |
| Company | Text | Manufacturer |
| Model | Text | Vehicle model |
| Engine | Text | Engine type |
| Transmission | Text | Auto / Manual |
| Color | Text | Vehicle color |
| Body Style | Text | Vehicle category |
| Price ($) | Currency | Sale price |
| Phone | Text | Contact number |

### Calendar Table

| Field | Type | Description |
|------|------|-------------|
| Date | Date | Calendar date |
| Month | Number | Month number |
| Week | Number | Week number |
| Year | Number | Calendar year |

---

## 💼 Business Value

This dashboard helps organizations:
- Track sales performance in near real-time
- Identify top-performing dealers and regions
- Understand customer and product preferences
- Monitor pricing trends and revenue growth
- Compare current performance with historical benchmarks
- Support strategic decisions in inventory and marketing

---