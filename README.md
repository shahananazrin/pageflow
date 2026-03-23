# 📚 PageFlow — Book Exchange & Marketplace System

A Django-based web application that enables users to **buy, sell, and exchange books** through a simple and intuitive platform. PageFlow is designed as a lightweight marketplace with core e-commerce and peer-to-peer exchange functionalities, making it ideal for academic and portfolio use.

---

## 📖 Description

**PageFlow** is a full-stack web application built using Django that allows users to:

* List books for sale or exchange
* Browse available books
* Send and manage exchange requests
* Review and rate transactions

The platform supports multiple user roles (buyers, sellers, and admin) and demonstrates key concepts such as authentication, relational database design, and request workflows.

---

## ✨ Features

* 🔐 User Authentication (Register/Login for Buyers & Sellers)
* 📚 Book Listing & Browsing
* 🔁 Book Exchange Request System
* ✅ Exchange Approval Workflow
* 📦 Delivery Confirmation (“Mark as Received”)
* ⭐ Rating System (1–5 stars)
* 💬 Comment & Review System
* 👤 Book Ownership (linked via Foreign Key to User)
* 🛠️ Admin Dashboard (Django Admin)
* 💳 Payment Success Page (Demo Implementation)

---

## 🛠️ Tech Stack

| Layer          | Technology           |
| -------------- | -------------------- |
| Backend        | Django (Python)      |
| Frontend       | HTML, CSS, Bootstrap |
| Database       | SQLite               |
| Authentication | Django Auth System   |

---

## ⚙️ Installation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/shahananazrin/pageflow.git
cd pageflow
```

### 2. Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate     # Linux/Mac
venv\Scripts\activate        # Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Create Superuser (Admin)

```bash
python manage.py createsuperuser
```

### 6. Run Development Server

```bash
python manage.py runserver
```

### 7. Open in Browser

```
http://127.0.0.1:8000/
```

---

## 🚀 Usage Instructions

### User Flow:

1. **Register/Login** as Buyer or Seller
2. **Browse Books** or **Add a New Book Listing**
3. **Send Exchange Request** for a book
4. **Owner Approves/Rejects Request**
5. Upon approval:

   * Proceed to **Payment (Demo Page)**
6. **Receiver Marks Book as Received**
7. Users can:

   * ⭐ Rate the transaction
   * 💬 Leave a review

---

## 📁 Project Structure

```
pageflow/
│── manage.py
│── db.sqlite3
│
├── pageflow/              # Main project settings
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
├── app/                   # Core application
│   ├── models.py          # Database models
│   ├── views.py           # Business logic
│   ├── urls.py            # App routes
│   ├── templates/         # HTML templates
│   └── static/            # CSS, JS, assets
│
└── requirements.txt
```

---

## 🗄️ Database Design Overview

### Key Entities:

* **User**

  * Stores authentication details
  * Roles: Buyer / Seller / Admin

* **Book**

  * Title, author, description
  * `owner_id` → Foreign Key to User

* **ExchangeRequest**

  * Requester → User
  * Book → Book
  * Status: Pending / Approved / Rejected

* **Review**

  * Rating (1–5 stars)
  * Comment
  * Linked to User & Book

* **Transaction**

  * Tracks exchange completion
  * Delivery confirmation status

---

## 🖼️ Screenshots

> *(Add screenshots here for better presentation)*

* Home Page
* Book Listings
* Exchange Request Page
* Admin Dashboard
* Review & Rating Section

---

## 🔮 Future Improvements

* 💳 Real Payment Gateway Integration (Stripe/Razorpay)
* 📱 Responsive UI Enhancements
* 🔍 Advanced Search & Filters
* 📦 Order Tracking System
* 📧 Email Notifications for Requests
* 🧠 Recommendation System (AI-based)
* 🌐 Deployment (AWS / Heroku / Vercel)

---

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to your branch
5. Open a Pull Request

---

## 📜 License

This project is for educational and demonstration purposes.
You may modify and use it for personal or academic projects.

---

## 🔗 Repository

GitHub:https://github.com/shahananazrin/pageflow
