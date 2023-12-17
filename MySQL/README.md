# MYSQL

## RoadMap

### Days 1-10: Basic Concepts and Setup
Day 1-2: Install MySQL on your machine. Create a simple database and table. \
Project
    Days 1-2: Database Setup Project
Day 3-5: Learn basic SQL queries (SELECT, INSERT, UPDATE, DELETE) and practice with your created table.\
Day 6-7: Explore data types in MySQL. Modify your table structure accordingly.\
Day 8-10: Study and implement basic normalization techniques. Adjust your table structure for better normalization.\

### Days 11-20: Advanced Queries
Day 11-12: Dive into JOIN operations. Practice INNER JOIN, LEFT JOIN, RIGHT JOIN on your existing tables.
Day 13-15: Work with aggregate functions like COUNT, SUM, AVG. Apply them to analyze your data.
Day 16-18: Practice subqueries. Create complex queries involving nested SELECT statements.
Day 19-20: Learn about indexing in MySQL. Apply indexing to improve query performance.

### Days 21-30: Stored Procedures and Triggers
Day 21-22: Create and execute your first stored procedure.
Day 23-25: Explore parameters and variables in stored procedures. Enhance the functionality of your procedures.
Day 26-28: Study and implement triggers. Create a trigger that responds to specific events on your tables.
Day 29-30: Combine stored procedures and triggers for a specific task.

### Days 31-40: Data Security and Transactions
Day 31-32: Understand user privileges and roles. Secure your database by assigning appropriate permissions.
Day 33-35: Implement transactions. Practice with COMMIT and ROLLBACK statements.
Day 36-38: Study and implement views. Create views to simplify complex queries.
Day 39-40: Explore and implement encryption techniques in MySQL.

### Days 41-50: Performance Optimization
Day 41-42: Use the EXPLAIN statement to analyze query execution plans. Optimize your queries based on the results.
Day 43-45: Study and implement caching mechanisms. Improve your database's overall performance.
Day 46-48: Practice using MySQL's built-in functions for performance optimization.
Day 49-50: Implement and test your own indexing strategy for specific queries.

### Days 51-60: Backup and Recovery
Day 51-52: Set up regular backups for your MySQL database.
Day 53-55: Practice restoring from backups. Simulate a recovery scenario.
Day 56-58: Explore MySQL dump and restore tools. Understand their use cases.
Day 59-60: Develop a comprehensive backup and recovery plan for your database.

### Days 61-70: Working with JSON and Spatial Data
Day 61-62: Learn about JSON functions in MySQL. Store and retrieve JSON data in your tables.
Day 63-65: Explore spatial data types and spatial indexing. Apply them to geographical data.
Day 66-68: Create queries that involve both JSON and spatial data.
Day 69-70: Develop a small project using JSON and spatial data in MySQL.

### Days 71-80: Data Warehousing and Analysis
Day 71-72: Understand data warehousing concepts. Design a simple data warehouse schema.
Day 73-75: Populate your data warehouse with relevant data.
Day 76-78: Create OLAP queries for data analysis.
Day 79-80: Visualize your analytical results using a reporting tool or language.

### Days 81-90: MySQL and Web Development
Day 81-82: Integrate MySQL with a web application. Use a server-side language like PHP or Node.js.
Day 83-85: Implement CRUD operations through your web application.
Day 86-88: Add user authentication and authorization to your web application.
Day 89-90: Optimize database queries for web application performance.


#### Days 91-100: Final Project and Review
Day 91-95: Plan and start working on a larger MySQL project. It could be a personal project or contribute to an open-source project.
Day 96-98: Refine and optimize your project. Implement any additional features.
Day 99: Perform a comprehensive review of your 100-day journey. Identify areas for further improvement.
Day 100: Celebrate your achievements and share your progress with the community.

# Projects
## Day 1: Basic Concepts and Setup

**Project Description:**
Your task for the first two days is to set up a basic MySQL database on your local machine. Follow the steps below to create a simple database and table.

**Instructions:**

1. **Install MySQL:**
   - Download and install MySQL on your machine. You can find installation instructions on the official MySQL website: [MySQL Downloads](https://dev.mysql.com/downloads/).

2. **Create a Database:**
   - Open MySQL Workbench or any MySQL client of your choice.
   - Execute the following SQL query to create a new database named `first_database`:
     ```sql
     CREATE DATABASE IF NOT EXISTS first_database;
     ```

3. **Create a Table:**
   - Within the newly created database, execute the following query to create a table named `first_table`:
     ```sql
     USE first_database;

     CREATE TABLE IF NOT EXISTS first_table (
         item_id INT AUTO_INCREMENT PRIMARY KEY,
         item_name VARCHAR(50) NOT NULL,
         quantity INT NOT NULL,
         price DECIMAL(10,2) NOT NULL,
         added_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
     );
     ```
   - This table stores information about items, including a unique item ID, item name, quantity, price, and a timestamp indicating when the item was added.

4. **Insert Sample Data:**
   - Populate the `first_table` table with sample data using the following query:
     ```sql
     INSERT INTO first_table (item_name, quantity, price) VALUES
         ('Widget A', 100, 5.99),
         ('Gadget B', 50, 12.50),
         ('Thingamajig C', 200, 2.25);
     ```
   - Feel free to add more sample data to the table.

## Day 2: Basic Concepts and Setup (Continued)

**Project Description:**
Today, your task is to independently set up a new MySQL database and design a table. Follow the detailed instructions below to create a database named `your_second_database` and design a table named `your_second_table` to manage information about books.

**Instructions:**

1. **Create a New Database:**
   - In your MySQL client, create a new database with the name `your_second_database`.

2. **Design a New Table:**
   - Within the newly created database, design a table named `your_second_table` to store information about books. Create the following columns:
     - `book_id`: This should be an integer, auto-incrementing, and set as the primary key.
     - `title`: A text field for the title of the book, with a maximum length of 100 characters and cannot be empty.
     - `author`: A text field for the author's name, with a maximum length of 50 characters and cannot be empty.
     - `publication_year`: An integer field for the year the book was published.
     - `price`: A decimal field with two decimal places for the price of the book, and it cannot be empty.

3. **Insert New Sample Data:**
   - Populate the `your_second_table` table with the following sample data:
     - Book: "The Catcher in the Rye"
       - Author: J.D. Salinger
       - Publication Year: 1951
       - Price: $14.99
     - Book: "Pride and Prejudice"
       - Author: Jane Austen
       - Publication Year: 1813
       - Price: $9.75
     - Book: "The Hobbit"
       - Author: J.R.R. Tolkien
       - Publication Year: 1937
       - Price: $12.50


---

### Day 3: Learn Basic SQL Queries

**Project Description:**
On Day 3, you will focus on learning basic SQL queries. Start by creating a new database named `your_third_database` and a table named `your_third_table`. Practice using SELECT, INSERT, UPDATE, and DELETE queries on this new table.

**Instructions:**

1. **Create a New Database:**
   - In your MySQL client, create a new database named `your_third_database`:
     ```sql
     CREATE DATABASE IF NOT EXISTS your_third_database;
     ```

2. **Create a New Table:**
   - Within the `your_third_database`, design a table named `your_third_table`. Choose a theme for this table (e.g., employees, products) and define meaningful columns with appropriate data types.
     ```sql
     USE your_third_database;

     CREATE TABLE IF NOT EXISTS your_third_table (
         employee_id INT AUTO_INCREMENT PRIMARY KEY,
         employee_name VARCHAR(50) NOT NULL,
         department VARCHAR(50),
         salary DECIMAL(10,2),
         hire_date DATE
     );
     ```

3. **Insert Sample Data:**
   - Populate the `your_third_table` with sample data using INSERT queries. Add records to the table based on the chosen theme.
     ```sql
     INSERT INTO your_third_table (employee_name, department, salary, hire_date) VALUES
         ('John Doe', 'IT', 60000.00, '2022-01-10'),
         ('Jane Smith', 'Marketing', 55000.00, '2022-02-15'),
         ('Bob Johnson', 'Finance', 70000.00, '2021-11-05');
     ```

4. **Practice Basic Queries:**
   - Execute basic SELECT, INSERT, UPDATE, and DELETE queries on `your_third_table`. Apply filters and conditions to retrieve, add, modify, and delete data.

   - **Example SELECT Queries:**
     - Retrieve all employees:
       ```sql
       SELECT * FROM your_third_table;
       ```

     - Retrieve employees in the IT department:
       ```sql
       SELECT * FROM your_third_table WHERE department = 'IT';
       ```

   - **Example INSERT Query:**
     - Add a new employee:
       ```sql
       INSERT INTO your_third_table (employee_name, department, salary, hire_date) VALUES
           ('Alice Brown', 'HR', 62000.00, '2022-03-20');
       ```

   - **Example UPDATE Query:**
     - Update salary for an employee:
       ```sql
       UPDATE your_third_table SET salary = 65000.00 WHERE employee_name = 'John Doe';
       ```

   - **Example DELETE Query:**
     - Remove an employee:
       ```sql
       DELETE FROM your_third_table WHERE employee_name = 'Jane Smith';
       ```


### Day 4: Explore Data Types and Modify Table Structure

**Project Description:**
Today's task is to independently set up a new MySQL database and design a table. Follow the detailed instructions below to create a database named `your_fourth_database` and design a table named `your_fourth_table` to manage information about products.

**Instructions:**

1. **Create a New Database:**
   - In your MySQL client, create a new database named `your_fourth_database`.
     ```sql
     CREATE DATABASE IF NOT EXISTS your_fourth_database;
     ```

2. **Design a New Table:**
   - Within the newly created database, design a table named `your_fourth_table` to store information about products. Create the following columns:
     - `product_id`: An integer, auto-incrementing, and set as the primary key.
     - `product_name`: A text field for the name of the product, with a maximum length of 100 characters and cannot be empty.
     - `stock_quantity`: An integer field for the quantity of the product in stock, and it cannot be empty.
     - `price`: A decimal field with two decimal places for the price of the product, and it cannot be empty.
     - `release_date`: A date field for the release date of the product.
     ```sql
     USE your_fourth_database;

     CREATE TABLE IF NOT EXISTS your_fourth_table (
         product_id INT AUTO_INCREMENT PRIMARY KEY,
         product_name VARCHAR(100) NOT NULL,
         stock_quantity INT NOT NULL,
         price DECIMAL(10,2) NOT NULL,
         release_date DATE
     );
     ```

3. **Insert New Sample Data:**
   - Populate the `your_fourth_table` table with the following sample data:
     - Product: "Laptop X"
       - Stock Quantity: 50
       - Price: $1200.00
       - Release Date: 2022-05-15
     - Product: "Smartphone Y"
       - Stock Quantity: 100
       - Price: $800.50
       - Release Date: 2022-03-10
     - Product: "Headphones Z"
       - Stock Quantity: 200
       - Price: $99.99
       - Release Date: 2022-07-01
     ```sql
     INSERT INTO your_fourth_table (product_name, stock_quantity, price, release_date) VALUES
         ('Laptop X', 50, 1200.00, '2022-05-15'),
         ('Smartphone Y', 100, 800.50, '2022-03-10'),
         ('Headphones Z', 200, 99.99, '2022-07-01');
     ```

4. **Update and Delete Activities:**
   - Execute UPDATE and DELETE queries on `your_fourth_table` to modify and remove sample data. For example:
     - Update the price of "Laptop X" to $1300.00.
     - Delete the record for "Headphones Z."
     ```sql
     UPDATE your_fourth_table SET price = 1300.00 WHERE product_name = 'Laptop X';
     DELETE FROM your_fourth_table WHERE product_name = 'Headphones Z';
     ```

