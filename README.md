# 💸 Expense Tracker & Analytics Dashboard

A full-stack **Expense Tracker & Analytics Dashboard** developed using **Python, Streamlit, and MySQL** to log, manage, and analyze daily personal finances, categorical spending, and historical expense trends through dynamic visualizations and secure multi-tenant access.

---

# 📊 Dashboard Preview

![Main Dashboard Preview](Dashboard%20Expense%20Tracker.png)

---

# 🎯 Project Objective

The objective of this project is to create a secure, multi-user web application that replaces manual financial tracking. It provides meaningful insights into personal spending habits, category-wise distributions, and daily expense trends through an interactive dashboard.

The dashboard helps users understand:
* Total Amount Spent
* Average Transaction Value
* Highest Spending Category
* Daily Spending Trends
* Categorical Expense Distribution
* Historical Financial Records

---

# 💼 Business Problem

Managing daily expenses manually using spreadsheets or physical notebooks is time-consuming, prone to calculation errors, and makes it difficult to identify long-term spending trends. Furthermore, tracking finances for multiple users on a single local machine usually leads to privacy issues and data overlap.

This dashboard transforms raw financial inputs into an interactive Business Intelligence solution, enabling users to log their data securely, explore historical records, and uncover valuable spending insights through automated visualizations.

---

# ❓ Key Analytical Questions

* What is the total amount spent within a specific month?
* Which category consumes the highest percentage of the budget?
* What is the average value of a daily transaction?
* How does spending fluctuate on a day-to-day basis?
* What are the historical expenses for a specific category like "Transport" or "Groceries"?
* How many active users and total entries are currently processed by the system?

---

# 🛠️ Tools & Technologies

* **Front-End:** Streamlit, HTML/CSS
* **Back-End:** Python 3
* **Database:** MySQL, `mysql-connector-python`
* **Data Visualization:** Plotly Express
* **Data Manipulation:** Pandas
* **Security & Auth:** Hashlib (SHA-256), `extra-streamlit-components` (Cookies)

---

# 📂 Dataset / Schema

The project uses a locally hosted relational MySQL database containing two primary tables:

**Users Table:**
* Username (Primary Key)
* Password Hash (SHA-256)

**Expenses Table:**
* Record ID (Primary Key)
* Expense Date
* Category
* Amount
* Description
* Username (Foreign Key link)

---

# 📈 Key Dashboard Metrics

| Metric                 | Description |
| ---------------------- | :--- |
| **Total Spent**        | Aggregate sum of filtered expenses |
| **Average Expense**    | Mean value of filtered transactions |
| **Top Category**       | Category with the highest total expenditure |
| **Registered Users**   | Live count of total system users |
| **Processed Entries**  | Live count of total database records |

---

# 📊 Dashboard Features

### 1. Multi-Tenant User Authentication
Secure login and sign-up portal utilizing SHA-256 password hashing and persistent 30-day browser cookies.

### 2. Interactive Analytics & Charts
Analyzes the percentage of total money spent across different categories (Pie Chart) and visualizes day-to-day spending spikes and trends (Bar Chart).

![Analytics Graphs](Graph%20Expenses%20Tracker.png)

### 3. Detailed Expense Records & CRUD Operations
Provides a clean, tabular view of all historical data, dynamically updating based on user filters. Users can seamlessly create new expense logs and delete erroneous entries directly from the interface using specific Record IDs.

![Data Records Tab](Data%20Records%20Expense%20Tracker.png)

### 4. Developer & System Telemetry
A dedicated portfolio tab displaying live database metrics, active registered users, total entries processed, and developer stack information.

![Developer Info Tab](Developer%20Inforamation%20Expenses%20Tracker.png)

---

# 🎛️ Interactive Filters

The dashboard includes dynamic Pandas-driven filters for customized analysis:
* Filter by **Month & Year** (e.g., September 2026)
* Filter by **Expense Category**

---

# 📁 Project Files

```text
Expense-Tracker-Streamlit/
│
├── app.py
├── .streamlit/
│   └── config.toml
├── sai image.png
├── Dashboard Expense Tracker.png
├── Data Records Expense Tracker.png
├── Developer Inforamation Expenses Tracker.png
├── Graph Expenses Tracker.png
└── README.md
