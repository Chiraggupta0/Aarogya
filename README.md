# 🏥 Aarogya - Hospital Management System

Aarogya is a console-based Hospital Management System built using **Java and MySQL**.  
It allows hospitals to manage patients, doctors, and appointments efficiently.

---

## 🚀 Features

- ➕ Add new patients  
- 📋 View all patients  
- 👨‍⚕️ View doctors  
- 📅 Book appointments  
- 🔍 Check doctor availability  
- 🔐 Secure database connection using Environment Variables  

---

## 🛠 Tech Stack

- Java (JDK 24)
- MySQL
- JDBC (MySQL Connector J)
- IntelliJ IDEA
- Git & GitHub

---

## 🗄 Database Setup

### 1️⃣ Create Database

```sql
CREATE DATABASE hospital;
```

### 2️⃣ Create Tables

```sql
CREATE TABLE patients (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    age INT,
    gender VARCHAR(10)
);

CREATE TABLE doctors (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    specialization VARCHAR(100)
);

CREATE TABLE appointments (
    id INT PRIMARY KEY AUTO_INCREMENT,
    patient_id INT,
    doctor_id INT,
    appointment_date DATE,
    FOREIGN KEY (patient_id) REFERENCES patients(id),
    FOREIGN KEY (doctor_id) REFERENCES doctors(id)
);
```

---

## 🔐 Environment Variables Setup (Important)

This project uses environment variables to securely store database credentials.

### 🔹 Windows (PowerShell)

```powershell
setx DB_URL "jdbc:mysql://localhost:3306/hospital"
setx DB_USERNAME "hospital_user"
setx DB_PASSWORD "your_password"
```

After setting variables:
- Restart IntelliJ
- Run the project again

---

## ▶ How to Run the Project

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/Aarogya.git
```

### 2️⃣ Open in IntelliJ IDEA

- Open the project folder
- Add MySQL Connector JAR to project libraries
- Set environment variables

### 3️⃣ Run

Run:

```
HospitalManagementSystem.java
```

---

## 📁 Project Structure

```
Aarogya/
│
├── src/
│   ├── HospitalManagementSystem.java
│   ├── Patient.java
│   └── Doctor.java
│
├── .gitignore
└── README.md
```

---

## 📈 Future Improvements

- GUI using JavaFX or Swing  
- Admin login system  
- Billing module  
- Prescription management  
- REST API version using Spring Boot  
- Docker deployment  

---

## 👨‍💻 Author

**Chirag Gupta**  
MCA Student | Java Backend Developer  

---

## ⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub!
