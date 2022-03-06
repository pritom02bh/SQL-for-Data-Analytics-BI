## SQL-for-Data-Analytics & Business Intelligence

MySQL Files &amp; Documentations                                                                   
***By Pritom Bhowmik***


### Data Definition Language (DDL)          
       - CREATE
       - ALTER
       - DROP
       - RENAME
       - TRUNCATE
            
### Data Manipulation Language (DML)
       - SELECT ... FROM
       - INSERT INTO ... VALUES
       - UPDATE ... SET ... WHERE
       - DELETE ... FROM ... WHERE
       
       
### Data Control Language (DCL)
       - GRANT
       - REVOKE
       
### Transaction Control Language (TCL)
       - COMMIT
       - ROLLBACK


NEW Authentication Plugin - Creating New User

                     --> cd C:\Program Files\MySQL\MySQL Server 8.0\bin
                     --> mysql -u root -p 1234pass
               mysql --> CREATE USER 'nativeuser'@'localhost'
                     --> IDENTIFIED WITH mysql_native_password BY '1234newpass';
                     Query OK......
               mysql --> GRANT ALL PRIVILGES ON *.* TO 'nativeuser'@'localhost';
              
