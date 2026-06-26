# 💳 Credit Card Financial Dashboard — Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)

An interactive, two-page Power BI dashboard that provides a comprehensive analysis of credit card transactions and customer demographics. Built to deliver actionable insights for financial stakeholders through real-time KPI monitoring and multi-dimensional revenue breakdowns.

---

## 📊 Dashboard Overview

The report consists of **2 pages**, each targeting a different analytical lens:

### Page 1 — Credit Card Transaction Analysis
Focuses on transaction-level data to track financial performance and spending patterns.

| Visual | Insight |
|--------|---------|
| 📈 Combo Chart | Quarterly Revenue vs. Total Transaction Count |
| 📊 Bar Charts | Revenue by Expenditure Type, Card Category, Chip Usage |
| 📊 Bar Chart | Revenue by Education Level & Customer Job |
| 🗺️ Tree Maps | Multi-dimensional breakdowns of transaction data |
| 🃏 KPI Cards | **Revenue**, **Total Transaction Amount**, **Total Interest Earned**, **Transaction Count** |

### Page 2 — Credit Card Customer Analysis
Focuses on customer demographics to understand who is driving revenue.

| Visual | Insight |
|--------|---------|
| 📊 Bar Charts | Revenue by Income Group, Age Group, Dependent Count, Marital Status, Education Level, Top 5 States |
| 📈 Line Chart | Weekly Revenue Trend (segmented by Gender) |
| 🗺️ Tree Maps | Demographic revenue distribution |
| 🃏 KPI Cards | **Revenue**, **Total Income**, **Total Interest Earned**, **Customer Satisfaction Score (CSS)** |

---

## 🗃️ Data Model

The dashboard is powered by two tables sourced from a **PostgreSQL** database (`public` schema):

### `cc_detail` — Transaction Table
| Column | Description |
|--------|-------------|
| `revenue` | Total revenue generated per transaction |
| `total_trans_amt` | Sum of transaction amounts |
| `total_trans_ct` | Count of transactions |
| `interest_earned` | Interest earned per account |
| `card_category` | Card tier (Blue, Silver, Gold, Platinum) |
| `exp_type` | Expenditure type (Bills, Entertainment, Food, etc.) |
| `use_chip` | Payment method (Chip, Swipe, Online) |
| `qtr` | Quarter of transaction |
| `week_start_date` | Weekly date hierarchy for time-series analysis |

### `cust_detail` — Customer Table
| Column | Description |
|--------|-------------|
| `income` | Customer annual income |
| `income_group` | Grouped income bucket |
| `age_group` | Age bracket |
| `education_level` | Highest education attained |
| `customer_job` | Customer occupation |
| `marital_status` | Marital status |
| `dependent_count` | Number of dependents |
| `state_cd` | US state code |
| `gender` | Customer gender |
| `cust_satisfaction_score` | Customer satisfaction score (CSS) |

---

## ⚙️ Technical Stack

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard design, DAX measures, report publishing |
| **PostgreSQL** | Backend data source (`public.cc_detail`, `public.cust_detail`) |
| **DAX** | Custom KPI measures (Revenue, Interest, Transaction Count, CSS) |
| **Power Query (M)** | Data transformation and loading |

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/Abhishek-Nayak-2004/<repo-name>.git
   ```

2. **Open the file** — Open `Dashboard.pbix` in **Power BI Desktop** (free download from Microsoft).

3. **Connect to your data source**
   - Go to **Home → Transform Data → Data Source Settings**
   - Update the PostgreSQL server and database credentials to match your environment
   - Alternatively, import the provided CSV/SQL files to recreate the tables locally

4. **Refresh the data** — Click **Refresh** on the Home ribbon to load the latest data.

---

## 📸 Screenshots

> *(Add screenshots of your dashboard pages here)*
>
> `Page 1 - Transaction Analysis`  
> `Page 2 - Customer Analysis`

---

## 💡 Key Insights Surfaced

- Identified **top revenue-generating card categories** and expenditure types
- Tracked **quarterly revenue trends** alongside transaction volume fluctuations
- Segmented customer revenue by **income group, age, education, and geography**
- Monitored **weekly revenue trends by gender** for targeted marketing decisions
- Measured **customer satisfaction scores** alongside financial performance

---

## 🧠 Skills Demonstrated

- Data modeling with relational tables in Power BI
- Writing DAX measures for KPIs (SUM, aggregations)
- Designing multi-page interactive dashboards with slicers and cross-filtering
- Connecting Power BI to a PostgreSQL backend
- Business storytelling through data visualization

---

## 📁 Repository Structure

```
📦 credit-card-dashboard
 ┣ 📊 Dashboard.pbix       # Power BI report file
 ┣ 📄 README.md            # Project documentation
 ┗ 📂 data/                # (Optional) Sample data files / SQL scripts
```

---

## 👤 Author

**Abhishek Nayak**  
GitHub: [@Abhishek-Nayak-2004](https://github.com/Abhishek-Nayak-2004)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
