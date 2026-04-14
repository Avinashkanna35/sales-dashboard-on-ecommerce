# 🛒 E-Commerce Sales Dataset — Analysis & Documentation

![Platform](https://img.shields.io/badge/Domain-E--Commerce-blue)
![Country](https://img.shields.io/badge/Country-India-orange)
![Records](https://img.shields.io/badge/Records-200-green)
![Sheets](https://img.shields.io/badge/Sheets-7-purple)

A comprehensive multi-sheet Excel dataset capturing e-commerce sales transactions across major Indian cities and platforms. Includes order-level data, monthly sales breakdowns, profit calculations, return types, and pivot summaries — suitable for sales analytics, business intelligence dashboards, and machine learning projects.

<img width="1418" height="524" alt="Screenshot 2026-04-14 132922" src="https://github.com/user-attachments/assets/73fef931-f81c-4747-b6da-0634ec0496a0" />

---

## 📁 File Structure

```
ecommerce_sales_dataset.xlsx
├── master_data       → Core order records (200 rows × 26 columns)
├── Input_data1       → Vendor-level aggregated data
├── Input_data3       → Extended dataset with state, return type, monthly breakdowns
├── input_data        → Computed profit & percentage metrics per city/month
├── Analysis          → Pivot summaries (return type × platform quantities)
├── pivot_tables      → City-wise sales & profit pivot tables
└── dash_bord         → Dashboard control sheet
```

---

## 📊 Dataset Overview

| Attribute             | Detail                                      |
|-----------------------|---------------------------------------------|
| **Total Records**     | 200 orders                                  |
| **Total Revenue**     | ₹5,12,641                                   |
| **Total Cost**        | ₹3,08,619                                   |
| **Total Profit**      | ₹1,94,667                                   |
| **Overall Profit Margin** | 37.97%                                 |
| **Avg. Discount**     | 15.48%                                      |
| **Avg. Delivery Time**| 5.14 days                                   |
| **Geography**         | 5 Indian cities across 5 states             |
| **Platforms**         | Amazon, Flipkart, Snapdeal, AJIO            |

---

## 🗂️ Schema — `master_data` (Primary Sheet)

| Column | Type | Description |
|---|---|---|
| `Order_ID` | string | Unique order identifier (e.g., ORD1000) |
| `Customer_ID` | string | Customer identifier (e.g., CUST202) |
| `City` | string | City of the order |
| `Category` | string | Product category (Electronics, Fashion, Beauty, Home) |
| `Product_Name` | string | Product identifier (Product_A to Product_D) |
| `Unit_Price` | float | Price per unit (₹15.98 – ₹498.87) |
| `Discount (%)` | float | Discount applied (0.01% – 29.98%) |
| `Revenue` | float | Order revenue after discount |
| `Cost` | float | Order cost |
| `Profit` | float | Revenue minus cost |
| `Payment_Method` | string | Cash on Delivery / UPI / Credit Card / Debit Card |
| `Delivery_Time (Days)` | int | Delivery duration (1–9 days) |
| `Platform` | string | Selling platform |
| `Jan_Sales` – `Dec_Sales` | int | Monthly unit sales figures |

---

## 📈 Key Insights

### 🏷️ Category Performance

| Category | Revenue (₹) | Profit (₹) | Avg. Margin |
|---|---|---|---|
| Electronics | 1,64,968 | 64,082 | 78.2% |
| Home | 1,27,430 | 40,366 | 64.5% |
| Fashion | 1,15,070 | 45,730 | 96.4% |
| Beauty | 1,05,173 | 44,489 | **133.6%** |

> 💡 **Beauty** has the highest profit margin despite lowest revenue — suggesting strong pricing power or low production cost.

---

### 🌐 Platform Performance

| Platform | Revenue (₹) |
|---|---|
| Snapdeal | 1,46,818 |
| AJIO | 1,28,377 |
| Flipkart | 1,19,560 |
| Amazon | 1,17,886 |

> Snapdeal leads by revenue; all four platforms are closely competitive.

---

### 🏙️ City-wise Profit

| City | Profit (₹) |
|---|---|
| Mumbai | 42,755 |
| Chennai | 42,596 |
| Hyderabad | 40,684 |
| Bangalore | 36,176 |
| Delhi | 32,457 |

---

### 💳 Payment Method Distribution

| Method | Orders |
|---|---|
| Cash on Delivery | 59 (29.5%) |
| UPI | 58 (29.0%) |
| Credit Card | 44 (22.0%) |
| Debit Card | 39 (19.5%) |

> COD and UPI dominate, reflecting typical Indian e-commerce consumer behaviour.

---

### 📅 Monthly Sales Trend

| Month | Sales Units |
|---|---|
| Jan | 52,90,374 |
| Feb | 52,41,674 |
| Mar | 53,58,484 ↑ |
| Apr | 52,84,275 |
| May | 51,25,081 |
| Jun | 51,16,527 |
| Jul | 51,29,855 |
| Aug | 52,19,142 |
| Sep | 50,80,906 |
| Oct | 50,55,445 ↓ |
| Nov | 51,55,607 |
| Dec | 53,68,759 ↑ |

> March and December show the highest sales — likely driven by end-of-quarter activity and festive season shopping.

---

### 🔄 Return & Exchange Types

| Type | Count |
|---|---|
| Exchanges | 63 (31.5%) |
| Warranties | 47 (23.5%) |
| Replacements | 46 (23.0%) |
| Refunds | 44 (22.0%) |

---

## 💡 Potential Use Cases

- **Sales Forecasting** — monthly time-series data per product/city
- **Customer Segmentation** — by city, payment method, platform
- **Profitability Analysis** — discount impact on margins
- **Return Rate Analytics** — by category, platform, return type
- **Dashboard Building** — ready-made pivot and analysis sheets included
- **ML Classification** — predict payment method or return type from order features

---

## 🗺️ Geographic Coverage

| City | State |
|---|---|
| Delhi | Delhi |
| Chennai | Tamil Nadu |
| Bangalore | Karnataka |
| Mumbai | Maharashtra |
| Hyderabad | Telangana |

---

## ✅ Data Quality

- **Missing values**: None (all 200 rows × 26 columns are complete in `master_data`)
- **Duplicates**: No duplicate Order IDs detected
- **Data types**: Consistent — numeric fields are float/int, categoricals are strings
- **Date coverage**: Full 12-month annual cycle (Jan–Dec)

---

## 📌 Notes

- Product names are anonymised (`Product_A` through `Product_D`)
- Customer IDs are pseudonymised (`CUST###`)
- All monetary values are in **Indian Rupees (₹)**
- The `input_data` sheet contains derived profit percentage calculations per city per month
- The `dash_bord` sheet is a control sheet for Excel slicers/dashboard — may not contain raw data

---

## 📄 License

This dataset is intended for educational and analytical purposes.
