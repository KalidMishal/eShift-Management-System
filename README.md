# eShift-Management-System
The **eShift Management System** is a desktop-based application built using   **C# (.NET Framework)** and **SQL Server LocalDB** to manage transport booking,   job handling, load assignments, and admin approval operations for a household shifting service.
---
https://drive.google.com/file/d/1N8kn94_u9T6_UQzBX96MPs5Txk0cWA7W/view?usp=sharing (Eshift system Zip File)
https://drive.google.com/file/d/1Bz267XnuRrngHCyMu9UWayLBoKKqR2dz/view?usp=sharing (Database File)

## 📌 Features

### 🔑 **Login & Authentication**
- Secure login for **Admin** and **Customer**
- Passwords stored using **SHA-256 hashing**
- Customers can sign up, but Admin has a fixed login

### 👨‍💼 Admin Features
- Admin dashboard with system controls  
- Add transport units (Lorry No, Driver, Assistant, Container Type)  
- Assign transport units to loads  
- Approve or reject load requests  
- View all customers, jobs, and loads  

### 👤 Customer Features
- Customer dashboard with personalized welcome  
- Register personal details  
- Create jobs (Start Location, Destination, Job Date)  
- Add loads related to each job  
- Update or delete load records  
- View their booking approval status  
- Send transport request  

---

## 🗂️ Database Structure

### **Tables Used**
- `Users`
- `Customers`
- `Jobs`
- `Loads`
- `TransportUnits`
- `LoadAssignments`

The database file **eShiftDB.mdf** is included inside the project folder under *App_Data*.

---

## 🔗 Database Connection

Uses LocalDB connection string (App.config):

```xml
<connectionStrings>
  <add name="eShiftDBConnectionString"
       connectionString="Data Source=(LocalDB)\MSSQLLocalDB;AttachDbFilename=|DataDirectory|\eShiftDB.mdf;Integrated Security=True"/>
</connectionStrings>

💻 Technology Stack
Frontend	C# Windows Forms
Backend	SQL Server LocalDB
Security	SHA-256 Password Hashing
IDE	Visual Studio 2022
Framework	.NET Framework 4.7.2

System Flow
Customer signs up → data stored in Users + Customers
Login → role-based dashboard redirection
**Customer can**
Register personal details
Create Jobs
Add Loads
View Booking status
**Admin can**
Add transport units
Assign transport
Approve or reject loads
All CRUD operations interact directly with SQL Server using SqlConnection + SQL queries

1️⃣ Clone the repo
git clone https://github.com/yourusername/eShift-Management-System.git

2️⃣ Open in Visual Studio
3️⃣ Restore Database

Open SQL Server Management Studio

Attach eShiftDB.mdf
OR
Run the scripts from SQL Scripts folder

4️⃣ Set Startup Project

Right-click → Set as Startup Project

5️⃣ Run the app 🎉
🔐 Default Admin Login
Username: Admin
Password: Admin123
Role: Admin
