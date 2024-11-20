
# JDBC CRUD - Student Records Management System 🎓📋

A Java-based Student Records Management System that utilizes **JDBC** for database interaction. This project allows users to perform **CRUD operations** (Create, Read, Update, Delete) on a database table that stores student information.

---

## Features ✨

1. **Create**:  
   - Add new student records to the database.
   
2. **Read**:  
   - View all student records or search for specific students by ID or name.

3. **Update**:  
   - Modify existing student records, such as updating names, grades, or contact details.

4. **Delete**:  
   - Remove student records from the database.

5. **Database Connectivity**:  
   - Utilizes JDBC (Java Database Connectivity) to connect to a MySQL (or other relational) database.

6. **Error Handling**:  
   - Handles database connection issues, invalid inputs, and SQL exceptions gracefully.

---

## How to Use 🕹️

### 1. Set Up the Database
- Create a database (e.g., `student_db`) in your SQL server.
- Use the following SQL script to create the `students` table:
  ```sql
  CREATE DATABASE student_db;

  USE student_db;

  CREATE TABLE students (
      id INT AUTO_INCREMENT PRIMARY KEY,
      name VARCHAR(50) NOT NULL,
      age INT NOT NULL,
      grade VARCHAR(5) NOT NULL,
      email VARCHAR(50)
  );
  ```

### 2. Configure Database Connection
- Update the database connection parameters in the Java code (e.g., `DB_URL`, `DB_USER`, `DB_PASSWORD`):
  ```java
  private static final String DB_URL = "jdbc:mysql://localhost:3306/student_db";
  private static final String DB_USER = "root";
  private static final String DB_PASSWORD = "password";
  ```

### 3. Run the Application
- Compile the code:
  ```bash
  javac StudentCRUDApp.java
  ```
- Run the application:
  ```bash
  java StudentCRUDApp
  ```

---

## Functionalities 🛠️

### 1. Add Student Record
- Enter student details such as name, age, grade, and email.
- The record will be inserted into the database.

### 2. View All Students
- Displays all student records from the database in a tabular format.

### 3. Search Student
- Search for a specific student by their ID or name.

### 4. Update Student Record
- Modify existing student information using the student ID as a reference.

### 5. Delete Student Record
- Remove a student record from the database using their ID.

---

## Example Usage 🎯

### Sample Menu
```text
Welcome to the Student Records Management System!

1. Add Student Record
2. View All Student Records
3. Search Student Record
4. Update Student Record
5. Delete Student Record
6. Exit

Enter your choice: 
```

### Input and Output
**Example Input**:  
Option: `1` (Add Student Record)  
Student Details:  
- Name: John Doe  
- Age: 21  
- Grade: A  
- Email: john.doe@example.com  

**Example Output**:  
```
Student record added successfully!
```

---

## Requirements 🛠️

- **Java Development Kit (JDK)**: Version 8 or later.
- **Database**: MySQL (or compatible database). Ensure MySQL Server is running.
- **JDBC Driver**: Ensure the appropriate JDBC driver (`mysql-connector-java`) is included in your project.

---

## Installation 🚀

1. Clone the Repository:
   ```bash
   git clone https://github.com/your-username/JDBC-CRUD-Student-Records.git
   cd JDBC-CRUD-Student-Records
   ```

2. Add JDBC Driver:
   - Download the MySQL Connector/J from [MySQL Downloads](https://dev.mysql.com/downloads/connector/j/).
   - Add it to your project's classpath.

3. Compile and Run:
   ```bash
   javac StudentCRUDApp.java
   java StudentCRUDApp
   ```

---

## To-Do List 📝

- Add support for exporting records to CSV or Excel.
- Implement input validation for better data integrity.
- Add GUI using Java Swing or JavaFX for better user experience.

---

## Contributing 🤝

Contributions are welcome! If you’d like to improve this project, please fork the repository and submit a pull request.

---

## License 📜

This project is licensed under the MIT License. See the `LICENSE` file for details.
