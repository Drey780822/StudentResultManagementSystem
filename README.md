# 🎓 Student Result Management System

A web-based application built using Java Enterprise technologies to manage student records and academic results.
The system provides role-based access for administrators and students, ensuring efficient and secure result management.

---

## 🚀 Overview

The **Student Result Management System** is designed to streamline the process of storing, managing, and accessing student academic results.

It allows:

* Administrators to manage student data and results
* Students to securely log in and view their academic performance

---

## 👥 Users

### 👨‍💼 Admin / Staff

* Manage student records
* Add, update, and delete results
* View all students and their performance

### 🎓 Students

* Log in securely using student credentials
* View personal results and grades

---

## ✨ Core Features

### 🔧 Admin Panel

* Add/Edit/Delete student records
* Add/Edit/Delete results per student
* View all students and their results

### 📊 Student Panel

* Secure authentication
* View individual results
* Simple and user-friendly dashboard

---

## 🛠️ Tech Stack

| Component | Technology                  |
| --------- | --------------------------- |
| Frontend  | HTML, CSS, JSP              |
| Backend   | Java (Servlets, JDBC / JPA) |
| Framework | Java EE (EJB)               |
| Database  | MySQL / Oracle DB           |
| Server    | Apache Tomcat / GlassFish   |
| Optional  | JSTL, Bootstrap             |

---

## 🏗️ System Architecture

The application follows the **MVC (Model-View-Controller)** architecture:

* **Model:** Java classes (Student, Result, DAO for database interaction)
* **View:** JSP pages (UI for login, dashboards, results)
* **Controller:** Servlets handling requests and business logic

---

## 🗄️ Database Design

### Students Table

```sql id="plwq1a"
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100),
    password VARCHAR(100)
);
```

### Results Table

```sql id="7p9t4d"
CREATE TABLE results (
    result_id INT PRIMARY KEY AUTO_INCREMENT,
    student_id INT,
    subject VARCHAR(100),
    marks INT,
    grade VARCHAR(2),
    FOREIGN KEY (student_id) REFERENCES students(student_id)
);
```

---

## 📄 Key Pages / Modules

| Page                    | Description          |
| ----------------------- | -------------------- |
| `index.jsp`             | Landing page         |
| `login.jsp`             | User authentication  |
| `admin-dashboard.jsp`   | Admin control panel  |
| `student-dashboard.jsp` | Student dashboard    |
| `add-student.jsp`       | Register new student |
| `add-result.jsp`        | Add student results  |
| `view-result.jsp`       | View results         |

### ⚙️ Core Servlets

* `AuthServlet.java` → Handles authentication
* `ResultServlet.java` → Manages result operations

---

## ⚙️ Installation & Setup

1. Clone the repository:

```bash id="0rj3e2"
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
```

2. Open the project in your IDE (e.g. NetBeans / IntelliJ)

3. Configure your server:

* Apache Tomcat or GlassFish

4. Set up the database:

* Create a database in MySQL or Oracle
* Run the SQL scripts provided

5. Update database connection settings in your project

6. Run the application:

* Deploy to server
* Access via browser (e.g. `http://localhost:8080/project-name`)

---

## 🔐 Security Features

* User authentication (Admin & Student roles)
* Session-based access control
* Restricted access to sensitive data

---

## 💡 Future Improvements

* Role-based authorization (more granular control)
* Export results (PDF/Excel)
* GPA calculations and analytics
* REST API integration
* Improved UI/UX with modern frameworks

---

## 👨‍💻 Author

**Thabang Dikotope**
Computer Science Student | Aspiring Software Engineer

---

## 📌 Note

This project demonstrates the use of Java Enterprise technologies (JEE) in building scalable, role-based web applications following industry-standard architecture (MVC).
