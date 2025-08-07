# 💊 Medical Supply Management System

## 🩺 Overview

The **Medical Supply Management System** is a web-based application built with Flask to facilitate the efficient handling of medical inventory. It streamlines medicine tracking, supply coordination, and order processing for **pharmacies**, **sellers**, and **suppliers**, ensuring minimal paperwork and enhanced digital security.

---

## 🎯 Objectives

- Develop an intuitive, secure, and efficient supply management platform.
- Eliminate redundancy with a robust MySQL-backed database.
- Provide a responsive and user-friendly interface.
- Enable secure login and authentication.
- Ensure instant access to medicine and supplier data.
- Minimize manual paperwork with digital workflows.

---

## 🚀 Features

- 📦 **Inventory Management**: Add, update, and delete medicines and products.
- 🔐 **User Authentication**: Role-based secure login to prevent unauthorized access.
- 📧 **Order Management**: Submit and track medicine orders with email alerts.
- 🧠 **Database Automation**: Triggers to log insert/delete operations.
- 🖼️ **Responsive Design**: Built with HTML, CSS, JS, and Bootstrap for cross-device compatibility.
- 📊 **Centralized Database**: MySQL-powered backend for real-time storage and retrieval.
- 🔁 **Stored Procedure**: Predefined logic for retrieving posts and medicine records.

---

## 🛑 Limitations

- Manual data entry can be time-consuming.
- No official government database integrations (e.g., Aadhar).
- Full automation for logistics and billing not implemented.
- Data reliability may depend on user input accuracy.

---

## ⚙️ Technology Stack

### 💻 Frontend
- HTML
- CSS
- JavaScript
- Bootstrap

### 🖥️ Backend
- Python 3.7
- Flask
- SQLAlchemy ORM
- MySQL

### 🧰 Development Tools
- PyCharm Community Edition / Sublime Text 3
- AMPPS (v3.7)
- Web Browsers: Chrome, Internet Explorer
- OS: Windows 10

---

## 🧾 System Requirements

### Hardware
- Processor: Intel Core i3 or better
- RAM: 2 GB minimum
- Storage: 2.5 GB free space
- Display: 1366 x 768 or higher

### Software
- Python 3.7
- MySQL Server
- AMPPS or equivalent
- Flask and Python packages

---

## 🏗️ Installation Guide

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/medical-supply-management-system.git
   cd medical-supply-management-system
   ```

2. **Install Python Dependencies**
   ```bash
   pip install flask flask-sqlalchemy flask-mail
   ```

3. **Configure MySQL**
   - Create a MySQL database.
   - Update `config.json`:
     ```json
     {
       "params": {
         "local_uri": "mysql://username:password@localhost/db_name",
         "prod_uri": "mysql://username:password@host/db_name",
         "gmail_user": "your-email@gmail.com",
         "gmail_password": "your-email-password",
         "user": "admin_username",
         "password": "admin_password"
       }
     }
     ```

4. **Run the Application**
   ```bash
   python app.py
   ```
   Visit [http://localhost:5000](http://localhost:5000)

---

## 🗃️ Database Schema

### 📌 Tables

#### `medicines`
| Field   | Type     | Description         |
|---------|----------|---------------------|
| id      | Integer  | Primary key         |
| amount  | Integer  | Quantity in stock   |
| name    | String   | Medicine name       |
| medicines | String | Category / details  |
| products | String  | Product information |
| email   | String   | Associated user     |
| mid     | String   | Medicine ID         |

#### `posts`
| Field       | Type     | Description        |
|-------------|----------|--------------------|
| mid         | Integer  | Primary key        |
| medical_name| String   | Medical store name |
| owner_name  | String   | Owner of the store |
| phone_no    | String   | Contact number     |
| address     | String   | Store address      |

#### `log`
| Field   | Type     | Description       |
|---------|----------|-------------------|
| id      | Integer  | Primary key       |
| mid     | String   | Medicine ID       |
| action  | String   | INSERT / DELETE   |
| date    | String   | Timestamp         |

---

## 🔁 Triggers

- `on_insert`: Logs every insert operation on `medicines`.
- `on_delete`: Logs every delete operation on `medicines`.

### 🧩 Stored Procedure

- `proc1_post_proc`: Retrieves all data from `posts` and `medicines` tables.

---

## 💼 Usage

- Visit: `http://localhost:5000`
- Login using credentials from `config.json`
- **Add medicines/products**: `/medicines`
- **View orders/list**: `/list`
- **Delete entries**: `/delete/<mid>`
- **Search/Add entries**: `/add`
- **Logout**: `/logout`

---

## 🚧 Future Enhancements

- Integration with government medical databases
- Transport & delivery module for logistics tracking
- Billing and payment gateway integration
- Improved user interface with dashboards
- Multilingual support

---

## 📚 References

- YouTube Tutorials
- Bootstrap Documentation
- Google Developer Resources

---

## 🤝 Contributing

We welcome contributions from the open-source community! Fork this repository, make your changes, and submit a pull request.

---

## 👩‍💻 Maintainer

HAJEERA SUHANI 
📧 hajirashariff25@gmail.com  
🔗 GitHub: (https://github.com/hajira25)
