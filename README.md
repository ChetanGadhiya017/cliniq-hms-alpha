# 🏥 Cliniq – The Intelligent Healthcare Platform

> A full-stack, role-based Hospital Management System built with modern web technologies.

---

## 🧩 Tech Stack

### ⚛ Frontend

* React
* React Router DOM
* Axios
* React Toastify
* Tailwind CSS
* Context API (State Management)

### 🌐 Backend

* Node.js
* Express.js
* MongoDB
* Mongoose
* JWT Authentication
* Role-based middleware

### 🛡 Security

* JWT-based authentication
* Secure password hashing (bcrypt)
* Role-based route protection

---

## 🚀 Project Overview

**Cliniq** is a web-based Health Management System designed to streamline hospital operations with secure, role-based access control.

The platform enables:

* 👨‍⚕ Doctors to manage appointments
* 🧑 Patients to book and track appointments
* 🛡 Admin to manage doctors and system-level data

The system is built with protected routing and role-based authentication to ensure secure and controlled access for each user type.

---

## 👥 Roles & Features

### 🧑 Patient

* Register & Login
* View list of available doctors
* Book appointment
* Cancel appointment
* View appointment status (Pending / Approved / Rejected)
* Dark/Light mode support

---

### 👨‍⚕ Doctor

* Secure login
* View own appointments only
* Approve appointment
* Reject appointment
* Manage profile (bio, specialization, photo)
* Dashboard with stats

---

### 🛡 Admin

* Create doctor accounts
* Manage system-level data
* Admin-only protected dashboard

---

## 🔐 Authentication & Security

* JWT-based authentication
* Role-based route protection
* Doctor sees only their appointments
* Admin-only protected routes
* Secure password hashing (bcrypt)

---

## 📂 Project Structure

```
cliniq-hms-alpha/
│
├── hms-frontend/
│   ├── src/
│   │   ├── pages/
│   │   ├── routes/
│   │   ├── context/
│   │   ├── services/
│   │   └── components/
│
├── hms-backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── utils/
│   └── server.js
```

---

## ⚙️ Installation Guide

### 1️⃣ Clone Repository

```bash
git clone https://github.com/yourusername/cliniq-hms-alpha.git
cd cliniq-hms-alpha
```

---

### 2️⃣ Backend Setup

```bash
cd hms-backend
npm install
```

Create `.env` file:

```
PORT=5000
MONGO_URI=your_mongodb_connection
JWT_SECRET=your_secret_key
```

Run backend:

```bash
npm run dev
```

Server runs at:

```
http://localhost:5000
```

---

### 3️⃣ Frontend Setup

```bash
cd hms-frontend
npm install
npm run dev
```

App runs at:

```
http://localhost:5173
```

---

## 🌐 Application Flow

### Landing Page

* Public homepage
* Login button in navbar

---

### Login Flow

* User selects role (Admin / Doctor / Patient)
* System auto redirects:

  * Admin → `/admin`
  * Doctor → `/doctor`
  * Patient → `/appointment`

---

### Register Flow

* New users register
* After registration → login required
* Role-based access control applied

---

## 🎨 UI Features

* Clean responsive layout
* Dark / Light mode toggle
* Toast notifications
* Modern dashboard UI
* Profile image support for doctors

---

## 🧠 Database Models

### User

* name
* email
* password
* role (admin / doctor / patient)

### Doctor

* user (ref to User)
* specialization
* bio
* photo

### Appointment

* patient (ref)
* doctor (ref)
* date
* timeSlot
* status (pending / approved / rejected / cancelled)

---

## 🔄 Appointment Workflow

1. Patient books appointment → Status = Pending
2. Doctor views appointments
3. Doctor approves or rejects
4. Patient sees updated status

---

## 📌 Current Status

✔ Authentication system complete
✔ Role-based access complete
✔ Doctor dashboard complete
✔ Appointment booking complete
✔ Profile management complete
✔ Theme toggle implemented
✔ Secure routing implemented

---

## 🚧 Future Improvements (Optional Enhancements)

* Real payment gateway integration (Stripe/Razorpay)
* File upload system (medical reports)
* Email notifications
* Doctor availability management
* Admin analytics dashboard
* Production deployment (Render/Vercel)
* Docker support
* API documentation with Swagger

---

## 🧪 Testing

Manual testing via:

* Postman (Backend APIs)
* Browser UI testing
* Role switching

---

## 📜 License

This project is built for academic and learning purposes.

---

## 🙌 Author

**Chetan Gadhiya**
Full Stack Developer | Computer Engineering Student

---

## ⭐ If You Like This Project

Give it a ⭐ on GitHub.

---

## 🏁 Final Note

This project demonstrates:

* Full-stack integration
* Role-based authentication
* Protected routing
* Clean architecture
* Context-based state management
* Secure backend design

This is a complete MVP-level Health Management System.

