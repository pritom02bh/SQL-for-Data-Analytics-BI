### Basic Operations on MYSQL --->

Creating a Database:                      
                       
                       CREATE DATABASE IF NOT EXIST Sales;
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
