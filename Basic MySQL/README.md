### Basic Operations on MYSQL --->

Creating a Database:                      
                       
                       CREATE DATABASE IF NOT EXISTS Sales;
                                      OR
                       CREATE SCHEMA IF NOT EXISTS Sales;
                     
Creating a table:
  
                        USE Sales;

                        CREATE TABLE sales
                        (
                            purchase_number INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
                            date_of_purchase DATE NOT NULL,
                            customer_id INT,
                            item_code VARCHAR(10) NOT NULL
                         );

                                   OR
                                    

                        CREATE TABLE sales
                        (
                          purchase_number INT NOT NULL AUTO_INCREMENT,
                          date_of_purchase DATE NOT NULL,
                          customer_id INT,
                          item_code VARCHAR(10) NOT NULL,
                        PRIMARY KEY (purchase_number)
                        );

FOREIGN KEY Constraint:           

                       USE sales;
			DROP TABLE sales;
			CREATE TABLE sales
			(
			    purchase_number INT AUTO_INCREMENT,
			    date_of_purchase DATE,
			    customer_id INT,
			    item_code VARCHAR(10),
			PRIMARY KEY (purchase_number),
			FOREIGN KEY (customer_id) REFERENCES customers(customer_id) ON DELETE CASCADE,
			FOREIGN KEY (item_code) REFERENCES items(item_code) ON DELETE CASCADE
			);
			

ADDING & DROPING FOREIGN KEY USING ALTER:

			USE sales;
			DROP TABLE sales;
			CREATE TABLE sales
			(
				purchase_number INT AUTO_INCREMENT,
			    date_of_purchase DATE,
			    customer_id INT,
			    item_code VARCHAR(10),
			PRIMARY KEY (purchase_number)
			);

			ALTER TABLE sales
			ADD FOREIGN KEY (customer_id) REFERENCES customers(customer_id) ON DELETE CASCADE;

			ALTER TABLE sales
			DROP FOREIGN KEY sales_ibfk_1;


UNIQUE KEY & INDEX:

Unique keys in MYSQL have the same role as indexes.
INDEX helps to retrieve data more easily.
	
ADDING A UNIQUE KEY:
			
			ALTER TABLE customers
			ADD UNIQUE KEY (email_address);

DROP UNIQUE KEY:
			
			ALTER TABLE customers
			DROP INDEX email_address;
