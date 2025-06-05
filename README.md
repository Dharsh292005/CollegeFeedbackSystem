# 🎓 College Feedback System – DBMS Project

## 📘 Project Overview

The **College Feedback System** is a database management system (DBMS) project that helps automate the process of collecting and managing student feedback on professors and courses. This system is intended to improve transparency and provide educational institutions with data-driven insights for quality enhancement.

---

## 🎯 Objectives

- Enable students to submit feedback securely and anonymously.
- Store and manage feedback records in a structured relational database.
- Allow admin access to view reports and analyze feedback data.
- Maintain data integrity using keys and relationships.

---

## 🏗️ System Design

### 🔑 Entities and Attributes

1. **Department**
   - `DeptID` (Primary Key)
   - `DeptName`

2. **Student**
   - `StudentID` (Primary Key)
   - `StudentName`, `Email`, `Phone`
   - `DepartmentID` (Foreign Key)

3. **Professor**
   - `ProfID` (Primary Key)
   - `ProfName`, `Email`, `Phone`
   - `DepartmentID` (Foreign Key)

4. **Feedback**
   - `FeedbackID` (Primary Key)
   - `FeedbackText`
   - `StudentID` (Foreign Key)
   - `ProfID` (Foreign Key)

5. **Report**
   - `ReportID` (Primary Key)
   - `ReportText`
   - `FeedbackID` (Foreign Key)

---

## 🔁 Relationships

- A **Department** has multiple **Students** and **Professors**.
- A **Student** gives feedback for multiple **Professors**.
- Each **Feedback** entry is linked to a single **Report**.
- All relationships are managed using **foreign keys**.

---

## ⚙️ Database Normalization

- ✅ First Normal Form (1NF): No multivalued or repeating attributes.
- ✅ Second Normal Form (2NF): Removed partial dependencies.
- ✅ Third Normal Form (3NF): Removed transitive dependencies.

---

## 💻 Technologies Used

- **Database:** MySQL
- **Frontend (optional):** HTML, CSS
- **Backend (optional):** PHP / Python / Node.js
- **Tools:** XAMPP, phpMyAdmin, VS Code

---

## 🧪 Sample SQL Queries

### Create Table Example:
```sql
CREATE TABLE Department (
  DeptID INT PRIMARY KEY,
  DeptName VARCHAR(100) NOT NULL
);
