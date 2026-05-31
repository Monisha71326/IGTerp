# 🏫 IGT ERP – Institute Management System

A web-based Institute ERP system built for managing all core operations of an IT training institute — using **Bootstrap 5 + Custom CSS** for UI and **plain JavaScript with fetch() API** for logic and Google Sheets integration.

---

## 📌 Project Overview

IGT ERP is a **frontend-only** admin dashboard system. All data is stored and retrieved via **Google Sheets** using **Google Apps Script Web App**.

> 🔐 Login session is managed via `localStorage` — no server required.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and markup |
| Bootstrap 5 | Responsive grid, components, layout |
| Custom CSS | Branding, colors, custom UI styles |
| JavaScript (Plain JS) | DOM manipulation, form handling, logic |
| fetch() API | Send/receive data to Google Sheets |
| Google Sheets | Backend database |
| Google Apps Script | Web App API (doGet / doPost) |
| Chart.js | Dashboard charts and analytics |
| Font Awesome | Icons throughout the UI |
| Google Fonts | Typography |

---

## 📸 Screenshots

### 🔐 Sign In Page
> `pages/sign-in.html`

![Sign In](docs/screenshots/signin.png)

---

### 📊 Dashboard
> `pages/dashboard.html`

![Dashboard](docs/screenshots/dashboard.png)

---

### 📋 Enquiry Management

#### Enquiry Form
> `pages/enquiry.html`

![Enquiry Form](docs/screenshots/enquiry-form.png)

#### Enquiry View
> `pages/enquiryview.html`

![Enquiry View](docs/screenshots/enquiry-view.png)

---

### 👨‍🎓 Student Management

#### Student Registration Form
> `pages/studentform.html`

![Student Form](docs/screenshots/student-form.png)

#### Student Records View
> `pages/studentview.html`

![Student View](docs/screenshots/student-view.png)

---

### 🧑‍🏫 Staff Management

#### Staff Registration Form
> `pages/staffregister.html`

![Staff Form](docs/screenshots/staff-form.png)

#### Staff Records View
> `pages/staffregisterview.html`

![Staff View](docs/screenshots/staff-view.png)

---

### 🗓️ Staff Attendance

#### Mark Staff Attendance
> `pages/attendence.html`

![Staff Attendance](docs/screenshots/staff-attendance.png)

#### Staff Attendance View
> `pages/attendenceview.html`

![Staff Attendance View](docs/screenshots/staff-attendance-view.png)

---

### 🎓 Student Attendance

#### Mark Student Attendance
> `pages/studentattendence.html`

![Student Attendance](docs/screenshots/student-attendance.png)

#### Student Attendance View
> `pages/studentattview.html`

![Student Attendance View](docs/screenshots/student-attendance-view.png)

---

### 💰 Payroll Management

#### Payroll Entry Form
> `pages/staffpayform.html`

![Payroll Form](docs/screenshots/payroll-form.png)

#### Payroll / Payslip View
> `pages/staffpayview.html`

![Payroll View](docs/screenshots/payroll-view.png)

---

### 💳 Billing Management

#### Billing Form
> `pages/billing.html`

![Billing Form](docs/screenshots/billing-form.png)

#### Billing Records View
> `pages/billingview.html`

![Billing View](docs/screenshots/billing-view.png)

---

### 📅 Batch Scheduling

#### Batch Entry Form
> `pages/batch.html`

![Batch Form](docs/screenshots/batch-form.png)

#### Batch Schedule View
> `pages/batchview.html`

![Batch View](docs/screenshots/batch-view.png)

---

### 📜 Student Certificate
> `pages/certificate.html`

![Certificate](docs/screenshots/certificate.png)

---

### 👤 Admin Profile
> `pages/profile.html`

![Profile](docs/screenshots/profile.png)

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

### Sample fetch() API Call

```javascript
const formData = {
  sheet: "Students",
  action: "insert",
  payload: { name: "Ravi", course: "Python", mobile: "9876543210" }
};

fetch(SHEET_API_URL, {
  method: "POST",
  body: JSON.stringify(formData)
})
.then(res => res.json())
.then(data => {
  alert("Student registered successfully!");
})
.catch(err => {
  console.error("Error:", err);
});
```

---

## ✨ Modules Overview

| # | Module | Files |
|---|---|---|
| 1 | Sign In | `sign-in.html` |
| 2 | Dashboard | `dashboard.html` |
| 3 | Enquiry Management | `enquiry.html`, `enquiryview.html` |
| 4 | Student Registration | `studentform.html`, `studentview.html` |
| 5 | Staff Registration | `staffregister.html`, `staffregisterview.html` |
| 6 | Staff Attendance | `attendence.html`, `attendenceview.html` |
| 7 | Student Attendance | `studentattendence.html`, `studentattview.html` |
| 8 | Payroll | `staffpayform.html`, `staffpayview.html` |
| 9 | Billing | `billing.html`, `billingview.html` |
| 10 | Batch Scheduling | `batch.html`, `batchview.html` |
| 11 | Certificate | `certificate.html` |
| 12 | Profile | `profile.html` |

---

## 📁 Project Structure

```
igterp/
│
├── pages/
│   ├── sign-in.html
│   ├── dashboard.html
│   ├── enquiry.html / enquiryview.html
│   ├── studentform.html / studentview.html
│   ├── staffregister.html / staffregisterview.html
│   ├── attendence.html / attendenceview.html
│   ├── studentattendence.html / studentattview.html
│   ├── staffpayform.html / staffpayview.html
│   ├── billing.html / billingview.html
│   ├── batch.html / batchview.html
│   ├── certificate.html
│   └── profile.html
│
├── assets/
│   ├── css/
│   │   ├── bootstrap.min.css
│   │   └── custom.css
│   ├── js/
│   │   ├── bootstrap.bundle.js
│   │   ├── chart.min.js
│   │   ├── config.js
│   │   └── app.js
│   ├── img/
│   └── fonts/
│
└── docs/
    ├── screenshots/
    │   ├── signin.png
    │   ├── dashboard.png
    │   ├── enquiry-form.png
    │   ├── enquiry-view.png
    │   ├── student-form.png
    │   ├── student-view.png
    │   ├── staff-form.png
    │   ├── staff-view.png
    │   ├── staff-attendance.png
    │   ├── staff-attendance-view.png
    │   ├── student-attendance.png
    │   ├── student-attendance-view.png
    │   ├── payroll-form.png
    │   ├── payroll-view.png
    │   ├── billing-form.png
    │   ├── billing-view.png
    │   ├── batch-form.png
    │   ├── batch-view.png
    │   ├── certificate.png
    │   └── profile.png
    └── documentation.html
```

---

## 🚀 Getting Started

### Prerequisites
- Any modern browser (Chrome, Firefox, Edge)
- Google account (for Google Sheets)
- No server setup needed

### Steps

1. **Clone the repo**
   ```bash
   git clone https://github.com/Monisha71326/igterp.git
   cd igterp
   ```

2. **Set up Google Sheets** with all tab names listed above

3. **Deploy Apps Script Web App** and copy URL to `assets/js/config.js`

4. **Open in browser**
   ```bash
   python -m http.server 8000
   # Visit: http://localhost:8000/pages/sign-in.html
   ```

---

## 👨‍💻 Author

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

[MIT License](https://opensource.org/licenses/MIT)
