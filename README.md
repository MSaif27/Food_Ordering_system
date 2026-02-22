# 🍽️ LPU Smart Food Stall Pre-Ordering System

A Django-based Smart Campus Food Management System with AI-powered demand prediction for Lovely Professional University.

---

## 📌 Project Overview

This system allows LPU students to pre-order food online, choose their preferred break time slot, and helps stall owners manage orders efficiently — reducing crowd congestion and waiting times.

---

## 🚀 Features

- Student registration & login
- Browse food menu by stall
- Pre-order food with break time slot selection
- Real-time order tracking
- Admin dashboard for stall owners
- Peak order time display
- **AI-based demand prediction** using Linear Regression (scikit-learn)

---

## 🛠️ Tech Stack

| Layer       | Technology                  |
|-------------|-----------------------------|
| Backend     | Django 4.2                  |
| Database    | MySQL                        |
| Frontend    | HTML, CSS, Bootstrap 5       |
| AI/ML       | scikit-learn, pandas, numpy  |
| Charts      | Chart.js                     |

---

## ⚙️ How to Run

### 1. Clone the repository
```bash
git clone <your-repo-url>
cd lpu_food_system
```

### 2. Create and activate virtual environment
```bash
python -m venv venv

# Windows
venv\Scripts\activate

# Mac/Linux
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure MySQL Database
- Open MySQL and create a database:
```sql
CREATE DATABASE lpu_food_db;
```
- Update `food_system/settings.py` with your MySQL credentials:
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'lpu_food_db',
        'USER': 'your_mysql_username',
        'PASSWORD': 'your_mysql_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

### 5. Run migrations
```bash
python manage.py makemigrations
python manage.py migrate
```

### 6. Create superuser (admin)
```bash
python manage.py createsuperuser
```

### 7. Load sample data (optional)
```bash
python manage.py loaddata sample_data.json
```

### 8. Run the server
```bash
python manage.py runserver
```

Visit: `http://127.0.0.1:8000`

---

## 📁 Project Structure

```
lpu_food_system/
│
├── food_system/          # Django project settings
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
├── orders/               # Main app
│   ├── models.py         # Database models
│   ├── views.py          # View logic
│   ├── urls.py           # App URLs
│   ├── forms.py          # Django forms
│   ├── ai_predictor.py   # AI demand prediction
│   └── admin.py          # Admin config
│
├── templates/            # HTML templates
│   ├── base.html
│   ├── home.html
│   ├── menu.html
│   ├── order.html
│   ├── dashboard.html
│   └── ...
│
├── static/               # CSS, JS, images
├── requirements.txt
└── manage.py
```

---

## 🤖 AI Demand Prediction

The system uses **Linear Regression** from scikit-learn to predict food demand based on:
- Historical order data
- Day of week
- Time slot
- Weather (optional)

Predictions help stall owners prepare the right quantity of food in advance.

---

## 👨‍💻 Author

- Student Name: [Your Name]
- Registration No: [Your Reg No]
- Course: Python and Full Stack — LPU
# AI-based_smart_attendance_system
