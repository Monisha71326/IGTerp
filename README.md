# 🏫 IGT ERP – Institute Management System

A web-based Institute ERP system to manage student enrollment, staff registration, course management, department & designation tracking, attendance monitoring, payroll processing, and certificate generation.

---

## 📌 Project Overview

IGT ERP is a **frontend-only HTML/CSS/JavaScript** dashboard system that provides a clean admin interface to manage an IT training institute's core operations.

> 🔐 Authentication is handled via `localStorage` — no server or database required.

---

## ✨ Features

### 📊 Dashboard
- Overview of Enquiry stats, Student Registrations, and Billing
- Enquiry Source Analysis charts (powered by Chart.js)
- Quick navigation to all modules

### 👨‍🎓 Student Management
- Register new students (`studentform.html`)
- View all student records in a table (`studentview.html`)

### 📚 Course Management
- Add new courses (`courseform.html`)
- View and manage existing courses (`courseview.html`)

### 🏢 Department Management
- Create departments (`department.html`)
- View department list (`departmentview.html`)

### 🪪 Designation Management
- Add designations/roles (`designationform.html`)
- View designation records (`designationview.html`)

### 👩‍💼 Staff Management
- Register staff members (`staffregister.html`)
- View all staff records (`staffregisterview.html`)

### 💰 Staff Payroll
- Add payroll entries (`staffpayform.html`)
- View payslips and salary records (`staffpayview.html`)

### 🗓️ Attendance Tracking
- Mark staff attendance (`attendence.html`)
- View attendance logs (`attendenceview.html`)
- Mark student attendance (`studentattendence.html`)
- View student attendance reports (`studentattview.html`)

### 🏅 Certificates
- Certificate display page with IGT branding
- Login-protected certificate viewer

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure |
| CSS3 + Bootstrap 5 | Styling and layout |
| JavaScript (Vanilla) | Logic, form handling, localStorage |
| Chart.js | Dashboard charts and analytics |
| Font Awesome | Icons |
| Google Fonts | Typography |

---

## 📁 Project Structure

```
igterp/
│
├── pages/                        # All main application pages
│   ├── sign-in.html              # Login page
│   ├── dashboard.html            # Main dashboard
│   ├── studentform.html          # Add student
│   ├── studentview.html          # View students
│   ├── courseform.html           # Add course
│   ├── courseview.html           # View courses
│   ├── department.html           # Add department
│   ├── departmentview.html       # View departments
│   ├── designationform.html      # Add designation
│   ├── designationview.html      # View designations
│   ├── staffregister.html        # Register staff
│   ├── staffregisterview.html    # View staff
│   ├── staffpayform.html         # Add payroll
│   ├── staffpayview.html         # View payroll
│   ├── attendence.html           # Staff attendance
│   ├── attendenceview.html       # View staff attendance
│   ├── studentattendence.html    # Student attendance
│   ├── studentattview.html       # View student attendance
│   ├── profile.html              # Admin profile
│   └── tables.html               # Data tables
│
├── certificate/                  # Certificate module
│   ├── login.html                # Certificate login
│   └── logo_files/               # Assets for certificate page
│
├── assets/
│   ├── css/                      # Styles
│   ├── js/                       # Core JS files
│   ├── img/                      # Images
│   └── fonts/                    # Icon fonts
│
└── docs/
    └── documentation.html        # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites
- Any modern web browser (Chrome, Firefox, Edge)
- No server setup needed — runs as static HTML

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/igterp.git
   ```

2. **Navigate into the project**
   ```bash
   cd igterp
   ```

3. **Open the login page**
   - Open `pages/sign-in.html` in your browser
   - Or use a local server:
     ```bash
     python -m http.server 8000
     ```
   - Then visit: `http://localhost:8000/pages/sign-in.html`

---

## 🔐 Login

The system uses `localStorage` for session management.

- Enter your credentials on the **Sign In** page (`pages/sign-in.html`)
- After successful login, `loggedIn` key is set in `localStorage`
- All protected pages redirect to login if this key is missing
- The **back button** is disabled after logout for security

---

## 📸 Screenshots

> *(Add screenshots of your dashboard, forms, and tables here)*

---

## 🧑‍💻 Author

**Monisha** — Developed as part of the IGT Institute ERP Project

---

## 📄 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## 📞 Contact

For any queries related to this project, reach out via GitHub Issues.
