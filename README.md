JavaFX Product Management System
Ved Patel – Student ID: 23094884
Lab Submission Date: July 3, 2025 Course: Programming concepts 2 Professor: stephen
📋 Overview
This project is a simple JavaFX desktop application that connects to a MySQL database. It allows users to log in and then perform view, insert, update, and delete operations on product records using a graphical interface.
⚙️ Technologies Used
•	Java 17 (or 11)
•	JavaFX (OpenJFX)
•	MySQL
•	JDBC (MySQL Connector/J)
•	Maven (for dependency management)
•	Replit (for development and testing)
•	XAMPP / phpMyAdmin (for local database)
✅ Features
•	User Login: Authenticates users against a users table in the database.
•	Product Management (CRUD):
o	View all product records in a TableView.
o	Insert new product records into the products table.
o	Update existing product information.
o	Delete products by ID.
•	Connects to MySQL via JDBC.
•	User-friendly GUI with buttons and text fields.
🚀 How to Run
1.	Database Setup:
o	Ensure you have MySQL installed (e.g., via XAMPP/MAMP).
o	Create a database named javafx_crud_db.
o	Execute the following SQL commands to create the users and products tables and insert sample data:
o	-- SQL for 'users' table (for login)
o	CREATE TABLE users (
o	    id INT AUTO_INCREMENT PRIMARY KEY,
o	    username VARCHAR(50) NOT NULL UNIQUE,
o	    password VARCHAR(255) NOT NULL, -- In a real app, hash passwords!
o	    role VARCHAR(20) DEFAULT 'user'
o	);
o	
o	INSERT INTO users (username, password, role) VALUES
o	('admin', 'adminpass', 'admin'),
o	('user1', 'userpass', 'user');
o	
o	-- SQL for 'products' table (for CRUD operations)
o	CREATE TABLE products (
o	    id INT AUTO_INCREMENT PRIMARY KEY,
o	    name VARCHAR(100) NOT NULL,
o	    price DECIMAL(10, 2) NOT NULL,
o	    quantity INT NOT NULL,
o	    description TEXT
o	);
o	
o	INSERT INTO products (name, price, quantity, description) VALUES
o	('Laptop', 1200.00, 10, 'Powerful laptop for everyday use.'),
o	('Mouse', 25.00, 50, 'Wireless ergonomic mouse.'),
o	('Keyboard', 75.00, 30, 'Mechanical gaming keyboard.');

o	Update the database connection details (DB_URL, DB_USER, DB_PASSWORD) in src/main/java/com/example/javafxcrudapp/util/DatabaseHandler.java to match your MySQL setup.
2.	Project Setup (Maven/Replit):
o	If using Maven locally, ensure you have Java 11 or 17 and Maven installed.
o	If using Replit:
	Create a new Java project.
	Recreate the directory structure as shown in the previous instructions (src/main/java/..., src/main/resources/...).
	Copy the Java source files (.java) and FXML files (.fxml) into their respective directories.
	Configure your pom.xml (or build.gradle) to include JavaFX and MySQL Connector/J dependencies. Replit's JavaFX template or specific configurations might be needed to run GUI applications.
3.	Build and Run:
o	Maven: Navigate to the project root in your terminal and run mvn clean javafx:run.
o	Replit: Use Replit's "Run" button, ensuring your pom.xml or .replit file is correctly configured to launch the JavaFX application.
📸 Screenshots
📷 Please add your screenshots below this section.
•	GUI Layout: Screenshots of the Login screen and the Product Management (CRUD) screen.
•	Database Table View: Screenshots from phpMyAdmin (or MySQL Workbench) showing the structure of your users and products tables, as well as sample data within them.
•	Relevant Code: Screenshots of key code sections (e.g., LoginController.java, ProductController.java, DatabaseHandler.java, App.java, LoginView.fxml, ProductView.fxml).
🔗 GitHub Repository
🔗 https://github.com/yourusername/JavaFX-Product-Management-System (Remember to replace yourusername/JavaFX-Product-Management-System with your actual GitHub repository link after uploading your project.)
🙏 Acknowledgments & Help
I would like to sincerely thank the following people for their help and guidance throughout this lab:
•	Preet Patel – Helped with Maven and JavaFX configuration
•	Piyush – Helped test and debug MySQL connection issues
•	ChatGPT – Used for guidance, code structuring, and error resolution
•	W3Schools and Stack Overflow – For syntax references and JavaFX layout tutorials
📚 References
•	JavaFX Documentation (OpenJFX)
•	MySQL Connector/J Docs
•	Replit JavaFX guide
•	Stack Overflow - JDBC Issues
