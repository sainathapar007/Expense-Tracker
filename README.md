# 💸 Daily Expense Tracker & Analytics Portal

A full-stack, multi-tenant web application designed to log, categorize, and visually analyze daily personal finances. This project demonstrates the integration of a responsive Python front-end with a relational SQL database, featuring secure user authentication and dynamic data visualization.

---

## 👨‍💻 About the Developer

**Sainath Apar**  
*Computer Science & Engineering Student | Dr. Babasaheb Ambedkar Technological University (DBATU)*

Focused on building scalable data-driven applications, relational database design, and integrating modern technologies. Passionate about bridging core concepts in Artificial Intelligence, Cloud Computing, and Big Data Analytics with practical, real-world utility software. 

* [LinkedIn Profile](https://www.linkedin.com/in/sainathapar)
* [GitHub Profile](https://github.com/sainathapar007)
* [Resume](https://drive.google.com/file/d/19EhDv1uXTF6J58FbwhUTCl8clD01zGa-/view?usp=drivesdk)
---

## 🚀 Key Engineering Features

* **Multi-Tenant Architecture:** Row-level security ensuring users can only read, update, and delete their own isolated financial data.
* **Secure Authentication:** Implements SHA-256 cryptographic hashing to securely store passwords rather than plain text.
* **Persistent Sessions:** Utilizes browser cookie management to maintain login states across page refreshes and browser closures.
* **Interactive Analytics:** Integrates Pandas for complex data aggregation and Plotly Express for rendering responsive, transparent-background pie and bar charts.
* **SQL Injection Defense:** All database interactions utilize parameterized queries (`%s`) to prevent malicious injection attacks.

---

## 💻 Technology Stack

* **Front-End:** Streamlit, HTML5/CSS3 (Custom UI rendering)
* **Back-End:** Python 3
* **Database:** MySQL, `mysql-connector-python`
* **Data Processing & Visualization:** Pandas, Plotly Express
* **Utilities:** Hashlib, `extra-streamlit-components` (Cookie Manager)

---

## 🛠️ Local Setup & Installation

If you would like to run this project locally, follow these steps:

### 1. Database Configuration
Launch MySQL Workbench and execute the following schema to initialize the database:

```sql
CREATE DATABASE expense_tracker;
USE expense_tracker;

CREATE TABLE users (
    username VARCHAR(50) PRIMARY KEY,
    password_hash VARCHAR(255) NOT NULL
);

CREATE TABLE expenses (
    id INT AUTO_INCREMENT PRIMARY KEY,
    expense_date DATE NOT NULL,
    category VARCHAR(50) NOT NULL,
    amount DECIMAL(10,2) NOT NULL,
    description VARCHAR(255),
    username VARCHAR(50) NOT NULL
);










## 2. Environment Setup
Clone the repository and install the required dependencies:

Bash
git clone [https://github.com/sainathapar007/Expense-Tracker-Streamlit.git](https://github.com/sainathapar007/Expense-Tracker-Streamlit.git)
cd Expense-Tracker-Streamlit
pip install streamlit mysql-connector-python pandas plotly extra-streamlit-components


3. Application Configuration
Open app.py.

Locate the get_connection() function.

Update the password field to match your local MySQL root password.






4. Launch the Application
Run the Streamlit server from your terminal:

Bash
streamlit run app.py




-----------------------------------------------------------------------------------------------



And this How your project also be ready to use





