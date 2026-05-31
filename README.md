# 🏫 IGT ERP – Institute Management System

A comprehensive Institute ERP application developed using HTML5, Bootstrap 5, Custom CSS, JavaScript, Google Sheets, and Google Apps Script.

## 📌 Project Overview

IGT ERP is designed to manage the day-to-day operations of a training institute through a centralized web-based dashboard.

### Key Features

- Student Enquiry Management
- Student Registration
- Course Management
- Department Management
- Designation Management
- Staff Registration
- Staff Attendance
- Student Attendance
- Payroll Management
- Billing & Fee Tracking
- Student Certificate Management
- Admin Dashboard

---

## 🛠️ Technology Stack

| Technology | Purpose |
|------------|----------|
| HTML5 | Structure |
| Bootstrap 5 | Responsive Layout |
| Custom CSS | Styling |
| JavaScript | Business Logic |
| Fetch API | Data Communication |
| Google Sheets | Database |
| Google Apps Script | Backend API |
| Font Awesome | Icons |
| Google Fonts | Typography |

---

# 🔐 Module 1 – Sign In

**File:** `pages/sign-in.html`

### Purpose
Provides authentication and access control.

### Features
- Login Authentication
- LocalStorage Session
- Password Toggle
- Logout Handling
- Protected Navigation

---

# 📊 Module 2 – Dashboard

**File:** `pages/dashboard.html`

### Purpose
Provides an overview of institute operations.

### Features
- Statistics Cards
- Student Overview
- Staff Overview
- Attendance Summary
- Quick Navigation Links

---

# 📋 Module 3 – Enquiry Management

**Files**
- `pages/profile.html`
- `pages/tables.html`

### Purpose
Capture and manage prospective student enquiries.

### Fields

| Field Name | Type |
|------------|------|
| Enquiry Date | Date |
| Student Name | Text |
| DOB | Date |
| Contact Number | Number |
| Email | Email |
| Address | Text |
| Course | Dropdown |
| Course ID | Auto Filled |
| Fees | Number |
| How Did You Know Us | Dropdown |
| Academic Details | Text |

### Functions
- Add Enquiry
- View Enquiries
- Edit Records
- Save to Google Sheets

---

# 👨‍🎓 Module 4 – Student Registration

**Files**
- `pages/studentform.html`
- `pages/studentview.html`

### Purpose
Register students and manage admission records.

### Fields

| Field Name | Type |
|------------|------|
| Student ID | Auto Generated |
| Student Name | Text |
| Mobile Number | Number |
| Email | Email |
| Course | Dropdown |
| Batch | Dropdown |
| Fees | Number |
| Paid Amount | Number |
| Balance Amount | Auto Calculated |
| Status | Active / Completed |

### Functions
- New Student Registration
- Student Record Management
- Admission Tracking
- Fee Tracking

---

# 💳 Module 5 – Billing Management

### Purpose
Integrated with Student Registration.

When students are registered, fee information is used for billing and payment tracking.

### Functions

- Fee Collection
- Balance Calculation
- Payment Tracking
- Receipt Management

---

# 📚 Module 6 – Course Management

**Files**
- `pages/courseform.html`
- `pages/courseview.html`

### Fields

| Field Name | Type |
|------------|------|
| Course Name | Text |
| Course ID | Text |
| Fees | Number |

### Functions

- Add Course
- Update Course
- View Courses

---

# 🏢 Module 7 – Department Management

**Files**
- `pages/department.html`
- `pages/departmentview.html`

### Fields

| Field Name | Type |
|------------|------|
| Department Name | Text |
| Department ID | Text |

---

# 🪪 Module 8 – Designation Management

**Files**
- `pages/designationform.html`
- `pages/designationview.html`

### Fields

| Field Name | Type |
|------------|------|
| Department | Dropdown |
| Designation | Text |
| Department ID | Text |

---

# 🧑‍🏫 Module 9 – Staff Registration

**Files**
- `pages/staffregister.html`
- `pages/staffregisterview.html`

### Functions

- Staff Registration
- Staff Record Management
- Qualification Tracking
- Salary Information
- Document Upload Management

### Fields

Employee ID, Full Name, Father Name, Mother Name, DOB, Gender, Mobile, Email, Department, Designation, Qualification, Experience, Salary, Bank Details and Supporting Documents.

---

# 🗓️ Module 10 – Staff Attendance

**Files**
- `pages/attendence.html`
- `pages/attendenceview.html`

### Features

- Daily Attendance
- In Time / Out Time
- Attendance Reports
- Staff Status Tracking

---

# 🎓 Module 11 – Student Attendance

**Files**
- `pages/studentattendence.html`
- `pages/studentattview.html`

### Features

- Student Attendance
- Batch Wise Attendance
- Attendance Reports
- Status Tracking

---

# 💰 Module 12 – Payroll Management

**Files**
- `pages/staffpayform.html`
- `pages/staffpayview.html`

### Features

- Salary Calculation
- Deduction Management
- Payroll Reports
- Payment Status

---

# 📜 Module 13 – Student Certificate Management

**Files**
- `pages/studentform.html`
- `pages/studentview.html`

### Purpose

Generate and maintain student certificate records.

### Fields

| Field Name | Type |
|------------|------|
| Student ID | Auto Generated |
| Student Name | Text |
| Course | Text |
| Certificate ID | Auto Generated |
| Issue Date | Date |

### Functions

- Certificate Generation
- Certificate Tracking
- Student Completion Records

---

# 👤 Module 14 – Admin Profile

**File**
- `pages/profile.html`

### Features

- Profile Information
- Admin Settings
- Account Management

---

# 📸 Screenshots

```text
docs/screenshots/
│
├── signin.png
├── dashboard.png
├── enquiry-form.png
├── enquiry-view.png
├── student-form.png
├── student-view.png
├── course-form.png
├── course-view.png
├── department-form.png
├── department-view.png
├── designation-form.png
├── designation-view.png
├── staff-form.png
├── staff-view.png
├── staff-attendance.png
├── staff-attendance-view.png
├── student-attendance.png
├── student-attendance-view.png
├── payroll-form.png
├── payroll-view.png
├── certificate.png
└── profile.png
```

---

# 🗄️ Database Architecture

Browser (HTML + JS)
↓
Fetch API
↓
Google Apps Script
↓
Google Sheets Database

---

# 📁 Project Structure

```text
igterp/
├── pages/
├── assets/
│   ├── css/
│   ├── js/
│   ├── img/
│   └── fonts/
└── docs/
    └── screenshots/
```

---

# 🚀 Getting Started

## Clone Repository

```bash
git clone https://github.com/Monisha71326/igterp.git
```

## Run Project

```bash
python -m http.server 8000
```

Open:

```text
http://localhost:8000/pages/sign-in.html
```

---

# 👨‍💻 Author

Monisha D

## Contact

GitHub: https://github.com/Monisha71326

LinkedIn: https://www.linkedin.com/in/monisha-d-8909a93b3

Email: iammonisha.dev@gmail.com

---

# 📄 License

MIT License
