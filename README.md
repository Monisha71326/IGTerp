# 🏫 IGT ERP – Institute Management System

A comprehensive **ERP (Enterprise Resource Planning)** web application built for **IGT (Institute of Global Technology)** to manage all day-to-day institute operations including students, staff, courses, attendance, and payroll — entirely through a browser with no backend required.

---

## 📌 Project Overview

IGT ERP is a **frontend-only HTML/CSS/JavaScript** dashboard system built on top of the **Argon Dashboard** UI framework. It provides a clean, role-based admin interface to manage an IT training institute's core operations.

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
| Argon Dashboard v2.1.0 | UI component framework |
| Chart.js | Dashboard charts and analytics |
| Font Awesome | Icons |
| Google Fonts | Typography |

---

## 📸 Screenshots

### 🔐 Sign In
![Sign In](docs/screenshots/signin.png)

---

### 📊 Dashboard
![Dashboard](docs/screenshots/dashboard.png)

---

### 📋 Enquiry Management
![Enquiry Form](docs/screenshots/enquiry-form.png)
![Enquiry View](docs/screenshots/enquiry-view.png)

---

### 👨‍🎓 Student Management
![Student Form](docs/screenshots/student-form.png)
![Student View](docs/screenshots/student-view.png)

---

### 📚 Course Management
![Course Form](docs/screenshots/course-form.png)
![Course View](docs/screenshots/course-view.png)

---

### 🏢 Department Management
![Department Form](docs/screenshots/department-form.png)
![Department View](docs/screenshots/department-view.png)

---

### 🪪 Designation Management
![Designation Form](docs/screenshots/designation-form.png)
![Designation View](docs/screenshots/designation-view.png)

---

### 👩‍💼 Staff Management
![Staff Form](docs/screenshots/staff-form.png)
![Staff View](docs/screenshots/staff-view.png)

---

### 🗓️ Staff Attendance
![Staff Attendance](docs/screenshots/staff-attendance.png)
![Staff Attendance View](docs/screenshots/staff-attendance-view.png)

---

### 🎓 Student Attendance
![Student Attendance](docs/screenshots/student-attendance.png)
![Student Attendance View](docs/screenshots/student-attendance-view.png)

---

### 💰 Payroll
![Payroll Form](docs/screenshots/payroll-form.png)
![Payroll View](docs/screenshots/payroll-view.png)

---

### 💳 Billing
![Billing Form](docs/screenshots/billing-form.png)
![Billing View](docs/screenshots/billing-view.png)

---

### 📅 Batch Scheduling
![Batch Form](docs/screenshots/batch-form.png)
![Batch View](docs/screenshots/batch-view.png)

---

### 📜 Certificate
![Certificate](docs/screenshots/certificate.png)

---

### 👤 Profile
![Profile](docs/screenshots/profile.png)

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
│   ├── css/                      # Argon dashboard styles
│   ├── js/                       # Core JS files
│   ├── img/                      # Images
│   └── fonts/                    # Icon fonts
│
└── docs/
    ├── screenshots/              # Page screenshots
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
   git clone https://github.com/Monisha71326/igterp.git
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

## 🗄️ Backend — Google Sheets as Database

```
Browser (HTML + Plain JS)
        ↓  fetch() POST / GET
Google Apps Script Web App (doGet / doPost)
        ↓
Google Sheets (Each module = one Sheet tab)
```

### Google Sheets Tab Structure

| Sheet Tab Name | Module It Serves |
|---|---|
| `Enquiry` | Enquiry Management |
| `Students` | Student Registration |
| `Staff` | Staff Registration |
| `StaffAttendance` | Staff Attendance |
| `StudentAttendance` | Student Attendance |
| `Payroll` | Staff Payroll |
| `Billing` | Student Billing |
| `Batches` | Batch Scheduling |
| `Certificates` | Certificate Log |

### Setup Steps

1. Create a new Google Sheet with the above tab names
2. Go to **Extensions → Apps Script**
3. Write `doGet()` and `doPost()` functions
4. Deploy as **Web App** → Access: **Anyone**
5. Copy the Web App URL into your project:

```javascript
// assets/js/config.js
const SHEET_API_URL = "https://script.google.com/macros/s/YOUR_SCRIPT_ID/exec";
```

---

## 🧑‍💻 Author

**Monisha** — Developed as part of the IGT Institute ERP Project

---

## 📞 Contact

| Platform | Details |
|---|---|
| 📱 Phone | [9940983824](tel:9940983824) |
| 📧 Email | [iammonisha.dev@gmail.com](mailto:iammonisha.dev@gmail.com) |
| 🐙 GitHub | [github.com/Monisha71326](https://github.com/Monisha71326) |

---

## 📄 License

This project uses the **Argon Dashboard** UI kit by [Creative Tim](https://www.creative-tim.com), licensed under the [MIT License](https://www.creative-tim.com/license).

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.
