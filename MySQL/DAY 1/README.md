Day 1: Basic Concepts and Setup
Project Description:
Your task for the first two days is to set up a basic MySQL database on your local machine. Follow the steps below to create a simple database and table.

Instructions:

Install MySQL:
Download and install MySQL on your machine. You can find installation instructions on the official MySQL website: MySQL Downloads.

Create a Database:
Open MySQL Workbench or any MySQL client of your choice.

Execute the following SQL query to create a new database named first_database:

sql
Copy code
CREATE DATABASE IF NOT EXISTS first_database;
Create a Table:
Within the newly created database, execute the following query to create a table named first_table:

sql
Copy code
USE first_database;

CREATE TABLE IF NOT EXISTS first_table (
    item_id INT AUTO_INCREMENT PRIMARY KEY,
    item_name VARCHAR(50) NOT NULL,
    quantity INT NOT NULL,
    price DECIMAL(10,2) NOT NULL,
    added_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
This table stores information about items, including a unique item ID, item name, quantity, price, and a timestamp indicating when the item was added.

Insert Sample Data:
Populate the first_table table with sample data using the following query:

sql
Copy code
INSERT INTO first_table (item_name, quantity, price) VALUES
    ('Widget A', 100, 5.99),
    ('Gadget B', 50, 12.50),
    ('Thingamajig C', 200, 2.25);
Feel free to add more sample data to the table.

# Projects
