### String Data Type

                        
          String Data Type             |   Storage  |     Example   |  Maximum size (bytes)  |       
         ------------------------------|------------|---------------|------------------------|----------------------------------------------------  
          character (CHAR)             |   fixed    |   CHAR(5)     |        255             | 50% faster
         ------------------------------|------------|---------------|------------------------|----------------------------------------------------    
          variable character(VARCHAR)  |  variable  |  VARCHAR(5)   |       65,535           | a lot more responsive to the data value inserted
         ------------------------------|------------|---------------|------------------------|----------------------------------------------------
          ENUM ("enumerate")           |   ENUM     | ENUM('M','F') |                        |
         ------------------------------|------------|---------------|------------------------|----------------------------------------------------- 
          
          Example:
            
          Company code (Must be 3 characters)         -->  company CHAR(3)
          Password (Can't be more than 10 characters) -->  password VARCHAR(10)
