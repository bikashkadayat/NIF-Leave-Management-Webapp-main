# NIF Leave Management System

A modern, role-based leave management system built with **Django REST Framework** (Backend) and **React + Vite** (Frontend). The system supports secure leave application, review, approval workflows, and team leave tracking through a clean and responsive interface.

---

## Features

* **Role-Based Access Control**

  * **Maker** → Apply for leave
  * **Checker** → Review leave requests
  * **Approver** → Approve or reject leave requests
  * **Admin** → Full system access

* **Leave Management**

  * Apply for leave
  * Track leave status
  * Manage leave history
  * Calendar-based leave visualization

* **User Registration**

  * Self-registration support
  * Automatic Maker role assignment

* **Team Calendar**

  * View approved leaves across the organization

* **Responsive UI**

  * Mobile-friendly modern interface

* **JWT Authentication**

  * Secure token-based login system

---

# Tech Stack

## Backend

* Python 3.8+
* Django 4.x
* Django REST Framework
* Simple JWT
* SQLite (Development)

## Frontend

* React 18
* Vite
* Axios
* React Router

## Styling

* Custom CSS
* CSS Variables

---

# Project Structure

```bash
leave-system/
├── backend/                 # Django backend
│   ├── config/              # Django settings
│   ├── users/               # User management app
│   ├── leaves/              # Leave management app
│   ├── db.sqlite3           # SQLite database
│   └── requirements.txt     # Python dependencies
│
├── frontend/                # React frontend
│   ├── src/
│   │   ├── components/      # Reusable components
│   │   ├── pages/           # Page components
│   │   ├── services/        # API services
│   │   └── hooks/           # Custom React hooks
│   ├── package.json         # Node dependencies
│   └── vite.config.js       # Vite configuration
│
└── README.md
```

---

# Backend Setup

## 1. Navigate to Backend Directory

```bash
cd backend
```

## 2. Create Virtual Environment

### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

### Windows

```bash
venv\Scripts\activate
```

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## 4. Run Migrations

```bash
python manage.py migrate
```

## 5. Create Superuser (Optional)

```bash
python manage.py createsuperuser
```

## 6. Run Development Server

```bash
python manage.py runserver
```

Backend will be available at:

```bash
http://localhost:8000
```

---

# Frontend Setup

## 1. Navigate to Frontend Directory

```bash
cd frontend
```

## 2. Install Dependencies

```bash
npm install
```

## 3. Start Development Server

```bash
npm run dev
```

Frontend will be available at:

```bash
http://localhost:5173
```

---

# Running the Full Application

## Start Backend

```bash
cd backend
source venv/bin/activate
python manage.py runserver
```

## Start Frontend

```bash
cd frontend
npm run dev
```

---

# Application URLs

| Service      | URL                             |
| ------------ | ------------------------------- |
| Frontend     | `http://localhost:5173`         |
| Backend API  | `http://localhost:8000/api/v1/` |
| Django Admin | `http://localhost:8000/admin/`  |

---

# User Roles

| Role     | Permission                       |
| -------- | -------------------------------- |
| Maker    | Apply for leave                  |
| Checker  | Review pending leave requests    |
| Approver | Approve or reject leave requests |
| Admin    | Full system access               |

---

# API Endpoints

## Authentication

| Method | Endpoint                 | Description           |
| ------ | ------------------------ | --------------------- |
| POST   | `/api/v1/auth/login/`    | User login            |
| POST   | `/api/v1/auth/register/` | User registration     |
| GET    | `/api/v1/auth/user/`     | Get current user info |

## Leave Management

| Method | Endpoint                          | Description          |
| ------ | --------------------------------- | -------------------- |
| GET    | `/api/v1/leaves/`                 | List leaves          |
| POST   | `/api/v1/leaves/`                 | Create leave request |
| POST   | `/api/v1/leaves/{id}/set_status/` | Update leave status  |
| GET    | `/api/v1/leaves/balance`          | Get leave balances   |
| GET    | `/api/v1/leaves/calendar`         | Team leave calendar  |

---

# Development

## Backend Commands

Run tests:

```bash
python manage.py test
```

Check project:

```bash
python manage.py check
```

Create migrations:

```bash
python manage.py makemigrations
```

---

## Frontend Commands

Build for production:

```bash
npm run build
```

Preview production build:

```bash
npm run preview
```

Run linter:

```bash
npm run lint
```

---

# Deployment

## Backend

* Set `DEBUG = False` in `config/settings.py`
* Configure PostgreSQL for production
* Set up static file serving
* Use Gunicorn or another production WSGI server

---

## Frontend

Build production files:

```bash
npm run build
```

Serve the generated `dist/` folder using any static hosting service.

Configure the production API base URL before deployment.

---

# Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests and lint checks
5. Submit a pull request

---

# License

This project is licensed under the MIT License.

---

# Support

For questions, issues, or feature requests, please create an issue in the repository.
