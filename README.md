# Account & Inventory Management System

FinSync is a full-stack Account and Inventory Management System designed to streamline business operations like purchase, sales, accounting, and reporting.
It supports multi-role authentication, real-time inventory tracking, financial accounting, and data analytics — built with modern technologies.

---

## 🚀 Tech Stack

* **Frontend:** React (Vite + TailwindCSS + ShadCN UI)
* **Backend:** Django (Python) + Django REST Framework
* **Database:** PostgreSQL
* **Authentication:** JWT-based secure login system

---

## 🧩 Core Features

|  # | Module                                    | Description                                                                                                                                                                                   |
| -: | :---------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|  1 | **User Authentication & Role Management** | Secure login system using JWT/OAuth. Supports **Admin**, **Accountant**, and **Staff** roles with role-based access control (RBAC). Ensures data confidentiality and multi-level permissions. |
|  2 | **Inventory Management**                  | Tracks stock inflow/outflow, generates **GRN (Goods Received Notes)**, manages damaged/returned goods, and updates real-time stock levels.                                                    |
|  3 | **Purchase & Sales Management**           | Handles purchase orders, supplier invoices, and customer bills. Automatically updates stock and generates journal entries for every transaction.                                              |
|  4 | **Journal Entry Management**              | Implements **double-entry bookkeeping**, automatically recording every credit/debit transaction according to accounting principles.                                                           |
|  5 | **Ledger Management**                     | Consolidates all journal entries per account type (**Assets, Liabilities, Income, Expenses**) with filters for date, category, or account name.                                               |
|  6 | **Profit & Loss Account**                 | Generates real-time Profit & Loss statements using sales, COGS, and expense data.                                                                                                             |
|  7 | **Balance Sheet Generation**              | Automatically prepares balance sheets showing Assets, Liabilities, and Equity for any accounting period.                                                                                      |
|  8 | **Cash Flow Management**                  | Records cash inflows and outflows from operational, investing, and financing activities to analyze liquidity.                                                                                 |
|  9 | **Reporting & Analytics**                 | Displays dynamic graphs and tables for sales trends, profit summaries, inventory aging, supplier performance, and tax data.                                                                   |
| 10 | **Audit Trail & Backup Management**       | Maintains a detailed log of every operation (add/edit/delete) for compliance and ensures secure data backup and recovery.                                                                     |

---

## ⚙️ Project Setup

### 🖥️ Frontend (React)

```bash
# Navigate to frontend folder
cd frontend

# Install dependencies
npm install

# Start development server
npm run dev
```

Frontend runs by default on:

👉 [http://localhost:5173](http://localhost:5173)

### 🐍 Backend (Django)

```bash
# Navigate to backend folder
cd backend

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # for Linux/Mac
venv\Scripts\activate     # for Windows

# Install dependencies
pip install -r requirements.txt

# Run migrations
python manage.py makemigrations
python manage.py migrate

# Create superuser (Admin)
python manage.py createsuperuser

# Start backend server
python manage.py runserver
```

Backend runs by default on:

👉 [http://127.0.0.1:8000](http://127.0.0.1:8000)

### 🗄️ Database (PostgreSQL)

Make sure PostgreSQL is installed and running.

Update your `backend/settings.py` file:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'fin_sync_aura_db',
        'USER': 'postgres',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

---

## 🔑 Environment Variables

Create a `.env` file inside your backend directory with:

```
SECRET_KEY=your_django_secret_key
DEBUG=True
DB_NAME=fin_sync_aura_db
DB_USER=postgres
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=5432
JWT_SECRET=your_jwt_secret
```

---

## 📡 API Endpoints (Example)

| Method | Endpoint                    | Description                    |
| :----: | :-------------------------- | :----------------------------- |
| `POST` | `/api/auth/login/`          | Login and receive JWT token    |
| `POST` | `/api/auth/register/`       | Register new user (Admin only) |
|  `GET` | `/api/inventory/`           | Get all inventory items        |
| `POST` | `/api/purchase/`            | Create new purchase entry      |
|  `GET` | `/api/ledger/`              | Fetch all ledgers              |
|  `GET` | `/api/reports/profit-loss/` | Get Profit & Loss report       |

---

## 📊 Dashboard Preview (Features)

* 📦 Real-Time Stock Overview
* 💰 Sales & Purchase Insights
* 🧾 Ledger Summary
* 📈 Profit Trends Visualization
* 🔒 User Role Permissions
* 🧮 Financial Statements Generator

---

## 🛠️ Folder Structure

```
fin-sync-aura-main/
│
├── frontend/                # React App (Vite + Tailwind)
│   ├── src/
│   ├── package.json
│   └── vite.config.js
│
├── backend/                 # Django REST API
│   ├── core/
│   ├── accounts/
│   ├── inventory/
│   ├── finance/
│   ├── manage.py
│   └── requirements.txt
│
├── README.md
└── .gitignore
```

---

## 🧠 Future Enhancements

* 🔐 Two-Factor Authentication (2FA)
* 📱 Mobile App (React Native)
* 🧾 GST & Tax Integration
* 🧰 AI-based Financial Forecasting
* ☁️ Cloud Backup & Deployment (AWS / Render)

