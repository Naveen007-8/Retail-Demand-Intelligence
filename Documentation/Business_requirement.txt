# Project Requirements
# Retail Demand Intelligence
### Integrating Sales, ERP Inventory and Marketing Metrics for Demand Forecasting and Replenishment


**Project Type:** End-to-End Data Analytics & Demand Forecasting  
**Target Audience:** Entry-Level Data Analyst / Business Analyst / Retail Analyst

---

## 1. Project Overview

The objective of this project is to develop an integrated retail analytics solution that combines historical sales, ERP-style inventory, purchase orders and marketing performance data.

The system will analyze historical product demand, identify inventory shortages and excess stock, evaluate marketing campaign performance, forecast future demand and recommend inventory replenishment decisions.

The final solution will include Python-based analytics, Oracle SQL database integration, machine-learning forecasting and an interactive Power BI dashboard.

## 2. Business Problem

Retail businesses face several operational challenges:

1. Frequent stockouts of high-demand products.
2. Excess inventory of slow-moving products.
3. Difficulty predicting future product demand.
4. Poor coordination between marketing campaigns and inventory availability.
5. Inefficient replenishment decisions.
6. Limited visibility into product and store-level performance.

### Proposed Solution

Build a centralized analytical workflow to:

- Analyze historical sales and demand patterns.
- Integrate ERP inventory and purchase order information.
- Evaluate marketing campaign performance.
- Forecast demand for the next 28 days.
- Calculate safety stock and reorder points.
- Recommend replenishment quantities.
- Provide actionable insights through Power BI.

---

## 3. Project Objectives

### Primary Objectives

1. Perform data extraction, cleaning and preprocessing.
2. Integrate sales, inventory, procurement and marketing datasets.
3. Perform exploratory data analysis.
4. Identify high-performing and slow-moving products.
5. Analyze seasonal and promotional demand.
6. Develop and evaluate demand forecasting models.
7. Calculate inventory optimization metrics.
8. Develop an interactive Power BI dashboard.
9. Generate business recommendations based on analytical findings.

### Expected Business Outcomes

- Better visibility into inventory health.
- Improved demand planning.
- Identification of potential stockout risks.
- Better replenishment decisions.
- Improved understanding of promotional demand patterns.
- Data-driven inventory management recommendations.

---

## 4. Software Requirements

| Software | Purpose | Priority |
|---|---|---|
| Python 3.11 | Main programming language | Required |
| Visual Studio Code | Development environment | Required |
| Jupyter Notebook | Interactive analysis | Required |
| Oracle Database XE | Relational database | Required |
| Oracle SQL Developer | Database query interface | Recommended |
| Power BI Desktop | Business intelligence dashboards | Required |
| Git | Version control | Required |
| GitHub | Portfolio and project repository | Required |
| Microsoft Excel | Dataset inspection and validation | Recommended |

### Software Installation

**Python:** https://www.python.org/downloads/

**VS Code:** https://code.visualstudio.com/

**Jupyter:** https://jupyter.org/

**Oracle Database XE:** https://www.oracle.com/database/technologies/xe-downloads.html

**Oracle SQL Developer:** https://www.oracle.com/database/sqldeveloper/

**Power BI Desktop:** https://www.microsoft.com/power-platform/products/power-bi/desktop

**Git:** https://git-scm.com/downloads

**GitHub:** https://github.com/

---

## 5. Python Library Requirements

The following libraries will support the project's data engineering, analytics, visualization and forecasting workflows.

### A. Data Manipulation and Processing

| Library | Purpose |
|---|---|
| pandas | Data cleaning, manipulation and integration |
| numpy | Numerical calculations and array operations |
| openpyxl | Excel file reading and writing |
| pyarrow | Efficient columnar data storage and Parquet files |

### B. Exploratory Data Analysis and Visualization

| Library | Purpose |
|---|---|
| matplotlib | Statistical and analytical visualizations |
| seaborn | Statistical visualization |
| plotly | Interactive charts |
| scipy | Statistical calculations and analysis |

### C. Machine Learning and Demand Forecasting

| Library | Purpose |
|---|---|
| scikit-learn | Regression, machine learning and model evaluation |
| statsmodels | Statistical analysis and time-series forecasting |
| scipy | Statistical methods and distributions |

### D. Database Connectivity

| Library | Purpose |
|---|---|
| oracledb | Python connectivity with Oracle Database |
| sqlalchemy | SQL database interaction and engine management |

### E. Development and Productivity

| Library | Purpose |
|---|---|
| jupyter | Notebook environment |
| ipykernel | Python kernel for Jupyter |
| python-dotenv | Environment variable management |
| tqdm | Progress monitoring |
| joblib | Saving and loading trained models |

### Python Dependency File

Create a file named `requirements.txt` in the project root:

```text
pandas>=2.2,<3.0
numpy>=1.26,<3.0
scikit-learn>=1.5,<2.0
statsmodels>=0.14,<1.0
scipy>=1.13,<2.0

matplotlib>=3.9,<4.0
seaborn>=0.13,<1.0
plotly>=5.24,<7.0

openpyxl>=3.1,<4.0
pyarrow>=17,<25

oracledb>=2.4,<4.0
sqlalchemy>=2.0,<3.0

jupyter>=1.1,<2.0
ipykernel>=6.29,<8.0

python-dotenv>=1.0,<2.0
tqdm>=4.66,<5.0
joblib>=1.4,<2.0
```

These are compatible version ranges, not a fully tested lockfile. Resolve and test the environment together before final deployment.

---

## 6. Python Environment Setup

### Step 1: Create project directory

```bash
mkdir Retail_Demand_Intelligence
cd Retail_Demand_Intelligence
```

### Step 2: Create virtual environment

```bash
python -m venv venv
```

### Step 3: Activate virtual environment

Windows:

```bash
venv\Scripts\activate
```

### Step 4: Upgrade pip

```bash
python -m pip install --upgrade pip
```

### Step 5: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 6: Register Jupyter kernel

```bash
python -m ipykernel install --user --name retail-demand-intelligence
```

### Step 7: Verify installation

```python
import pandas as pd
import numpy as np
import sklearn
import statsmodels
import matplotlib
import seaborn
import plotly
import oracledb
import sqlalchemy

print("All major project libraries imported successfully.")
print("Pandas:", pd.__version__)
print("NumPy:", np.__version__)
print("Scikit-learn:", sklearn.__version__)
print("Statsmodels:", statsmodels.__version__)
```

---

## 7. Dataset Requirements

### Primary Dataset: Walmart M5 Forecasting

Source:

https://www.kaggle.com/competitions/m5-forecasting-accuracy/data

Required source files:

1. sales_train_validation.csv
2. calendar.csv
3. sell_prices.csv

Purpose:

- Historical product sales.
- Product and store information.
- Calendar and holiday information.
- Product selling prices.
- Historical demand patterns.
- Forecasting model development.

### Supporting ERP Data

The public M5 dataset does not include actual ERP inventory or procurement records. We will create clearly labelled simulated datasets for practice.

Required simulated datasets:

1. inventory_snapshots.csv
2. inventory_movements.csv
3. purchase_orders.csv
4. supplier_master.csv
5. product_master.csv
6. store_master.csv

### Supporting Marketing Data

The marketing datasets will also be simulated.

Required datasets:

1. marketing_campaigns.csv
2. marketing_performance.csv

Suggested fields:

- Campaign_ID
- Campaign_Name
- Channel
- Start_Date
- End_Date
- Product_ID
- Advertising_Spend
- Impressions
- Clicks
- Conversions
- Attributed_Revenue

All simulated data must be explicitly documented as synthetic practice data, not actual Walmart records.

---

## 8. Database Requirements

**Database:** Oracle Database XE

### Required database components

- Sales staging tables.
- Product master.
- Store master.
- Inventory snapshots.
- Inventory movements.
- Purchase orders.
- Supplier master.
- Marketing campaign tables.
- Marketing performance tables.
- Integrated analytical tables.

### SQL skills required

- SELECT, WHERE and ORDER BY
- GROUP BY and HAVING
- INNER JOIN and LEFT JOIN
- Subqueries and CTEs
- CASE statements
- Aggregate functions
- Analytical/window functions
- Views
- Indexes
- Data validation and reconciliation

### Database design objective

Develop a relational database and a reporting-friendly dimensional model with appropriate fact and dimension tables.

---

## 9. Demand Forecasting Requirements

Forecasting must use historical demand observations and appropriate time-series validation.

### Forecasting approaches

1. Naive forecasting.
2. Seasonal naive forecasting.
3. Moving average.
4. Statistical time-series forecasting.
5. Machine-learning regression with lag and rolling features.

### Candidate models

- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- Suitable statistical forecasting models using Statsmodels

### Model evaluation metrics

- MAE
- RMSE
- WAPE
- Forecast Bias

### Forecasting requirements

- Use chronological training and testing.
- Apply rolling-origin validation where practical.
- Prevent data leakage.
- Compare complex models against simple baselines.
- Produce a 28-day forecast where appropriate.
- Document model assumptions and limitations.

Sales observations may be lower than true demand during stockouts. The analysis must not automatically interpret zero sales as zero customer demand.

---

## 10. Inventory Optimization Requirements

The project must calculate:

- Available inventory.
- Inventory position.
- Average daily demand.
- Lead-time demand.
- Safety stock.
- Reorder point.
- Days of supply.
- Replenishment quantity.
- Inventory turnover.

### Core formulas

**Inventory Position**

Inventory Position = On-hand Inventory + Incoming Inventory - Committed Inventory

**Reorder Point**

Reorder Point = Lead-time Demand + Safety Stock

**Days of Supply**

Days of Supply = Available Inventory / Average Daily Demand

**Replenishment Quantity**

Replenishment Quantity = Target Inventory Position - Current Inventory Position

The calculations must account for inventory commitments and incoming purchase orders, and document all service-level and supplier lead-time assumptions.

---

## 11. Power BI Requirements

Develop four dashboard pages.

### Page 1: Executive Retail Overview

- Total Sales
- Units Sold
- Revenue Trends
- Category Performance
- Store Performance
- Top Products

### Page 2: Demand Forecasting

- Actual vs Forecast Demand
- Forecast Accuracy
- Product-Level Forecast
- Demand Trends
- Seasonal Patterns

### Page 3: Inventory Optimization

- Inventory Position
- Stockout Risk
- Overstock Products
- Days of Supply
- Safety Stock
- Reorder Recommendations

### Page 4: Marketing Effectiveness

- Advertising Spend
- Impressions
- Clicks
- CTR
- CPC
- Conversion Rate
- ROAS
- Promotion-Related Demand Trends

---

## 12. Project Folder Structure

```text
Retail_Demand_Intelligence/
│
├── data/
│   ├── raw/
│   ├── simulated_erp/
│   └── processed/
│
├── Python/
│   ├── 01_Data_Cleaning.ipynb
│   ├── 02_Data_Integration.ipynb
│   ├── 03_Inventory_Analysis.ipynb
│   ├── 04_Marketing_Analysis.ipynb
│   ├── 05_Demand_Forecasting.ipynb
│   └── 06_Inventory_Optimization.ipynb
│
├── SQL/
│   ├── 01_Staging_Tables.sql
│   ├── 02_Data_Integration.sql
│   ├── 03_Demand_Analysis.sql
│   └── 04_KPI_Validation.sql
│
├── PowerBI/
│   └── Retail_Demand_Intelligence.pbix
│
├── models/
├── outputs/
├── documentation/
│   ├── Business_Requirements.md
│   ├── Data_Dictionary.md
│   ├── Data_Architecture.md
│   └── Final_Report.md
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## 13. Git and GitHub Requirements

The project must be maintained using Git.

Required practices:

- Initialize Git repository.
- Use meaningful commit messages.
- Maintain a `.gitignore` file.
- Document installation instructions.
- Include notebook outputs and screenshots where useful.
- Include architecture and data dictionary.
- Publish final source code and project documentation.

Do not upload passwords, credentials, virtual environments or restricted raw datasets.

---

## 14. Expected Final Deliverables

| Deliverable | Expected output |
|---|---|
| Data Cleaning | Clean and validated datasets |
| Data Integration | Combined analytical dataset |
| SQL Database | Staging and analytical tables |
| EDA | Sales, inventory and marketing analysis |
| Forecasting | Evaluated demand forecasting model |
| Inventory Optimization | Replenishment recommendations |
| Power BI | Four-page interactive dashboard |
| Documentation | Business requirements and technical report |
| GitHub | Reproducible portfolio repository |
| Presentation | Final business recommendations |

---

## 15. Project Success Criteria

The project will be considered complete when:

1. All required datasets are integrated and validated.
2. Data quality issues are documented.
3. SQL analysis produces reconciled results.
4. Forecasting models are compared using time-based validation.
5. Inventory optimization calculations are reproducible.
6. Marketing metrics are correctly defined.
7. All four Power BI pages are completed.
8. GitHub documentation is clear and reproducible.
9. Business recommendations are supported by analytical evidence.
10. All assumptions, simulated data and limitations are disclosed.

**Final Goal:** Deliver an end-to-end retail analytics solution demonstrating practical Python, Pandas, NumPy, Scikit-learn, Oracle SQL, Power BI, forecasting, inventory analytics and business decision-making skills.