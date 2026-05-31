# 🏫 IGT ERP – Institute Management System

A web-based Institute ERP system built using **HTML5, Bootstrap 5, Custom CSS, JavaScript, Google Sheets, and Google Apps Script**.

## 📌 Project Overview

IGT ERP is a frontend-based institute management application that helps manage:

- Student Enquiries
- Student Registration
- Course Management
- Department Management
- Designation Management
- Staff Registration
- Staff Attendance
- Student Attendance
- Staff Payroll
- Student Certificates
- Admin Profile

Google Sheets is used as the database through Google Apps Script APIs.

---

## 🛠️ Tech Stack

- HTML5
- Bootstrap 5
- Custom CSS
- JavaScript (ES6)
- Fetch API
- Google Sheets
- Google Apps Script
- Font Awesome
- Google Fonts

---

## 📂 Modules

### 🔐 Sign In
**File:** `pages/sign-in.html`

Features:
- Username & Password Login
- Local Storage Session
- Logout Protection
- Show / Hide Password

---

### 📊 Dashboard
**File:** `pages/dashboard.html`

Features:
- Quick Statistics
- Summary Cards
- Institute Overview

---

### 📋 Enquiry Management
**Files:**
- `pages/profile.html`
- `pages/tables.html`

Fields:
- Enquiry Date
- Student Name
- DOB
- Contact Number
- Email
- Address
- Course
- Course ID
- Fees
- How Did You Know Us
- Academic Details

---

### 👨‍🎓 Student Registration
**Files:**
- `pages/studentform.html`
- `pages/studentview.html`

Fields:
- Student ID
- Student Name
- Course
- Certificate ID
- Issue Date

---

### 📚 Course Management
**Files:**
- `pages/courseform.html`
- `pages/courseview.html`

Fields:
- Course Name
- Course ID
- Fees

---

### 🏢 Department Management
**Files:**
- `pages/department.html`
- `pages/departmentview.html`

Fields:
- Department Name
- Department ID

---

### 🪪 Designation Management
**Files:**
- `pages/designationform.html`
- `pages/designationview.html`

Fields:
- Department
- Designation
- Department ID

---

### 🧑‍🏫 Staff Registration
**Files:**
- `pages/staffregister.html`
- `pages/staffregisterview.html`

Fields:
- Employee ID
- Full Name
- Father Name
- Mother Name
- DOB
- Age
- Gender
- Mobile Number
- Email
- Address
- Aadhaar Number
- Department
- Designation
- Qualification
- Experience
- Previous Institute
- Salary
- Date of Joining
- Shift
- Bank Details
- Document Uploads

---

### 🗓️ Staff Attendance
**Files:**
- `pages/attendence.html`
- `pages/attendenceview.html`

Fields:
- Attendance ID
- Date
- Employee ID
- Employee Name
- Status
- In Time
- Out Time
- Remarks

---

### 🎓 Student Attendance
**Files:**
- `pages/studentattendence.html`
- `pages/studentattview.html`

Fields:
- Attendance ID
- Date
- Student ID
- Student Name
- Batch
- Status
- Remarks

---

### 💰 Staff Payroll
**Files:**
- `pages/staffpayform.html`
- `pages/staffpayview.html`

Fields:
- Payroll ID
- Employee ID
- Employee Name
- Salary
- Working Days
- Present Days
- Gross Salary
- Deductions
- Net Salary
- Payment Status

---

### 📜 Student Certificate
**Files:**
- `pages/studentform.html`
- `pages/studentview.html`

Fields:
- Student ID
- Student Name
- Course
- Certificate ID
- Issue Date

---

### 👤 Admin Profile
**File:** `pages/profile.html`

Features:
- Admin Information
- Profile Management

---

## 🗄️ Database Structure

Google Sheets is used as the backend database.

Suggested Sheets:

- Enquiry
- Students
- Courses
- Departments
- Designations
- Staff
- StaffAttendance
- StudentAttendance
- Payroll
- Certificates

---

## 📁 Project Structure

```text
igterp/
│
├── pages/
├── assets/
│   ├── css/
│   ├── js/
│   ├── img/
│   └── fonts/
│
└── docs/
    └── screenshots/
```

---

## 🚀 Getting Started

1. Clone the repository

```bash
git clone https://github.com/Monisha71326/igterp.git
```

2. Configure Google Apps Script

3. Add Web App URL in configuration

4. Run the project

```bash
python -m http.server 8000
```

Open:

```text
http://localhost:8000/pages/sign-in.html
```

---

## 👨‍💻 Author

**Monisha D**

---

## 📞 Contact

- GitHub: https://github.com/Monisha71326
- LinkedIn: https://www.linkedin.com/in/monisha-d-8909a93b3
- Email: iammonisha.dev@gmail.com

---

## 📄 License

MIT License
