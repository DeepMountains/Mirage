# Vendor

itsourcecode

# Product

University Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2022/01/University-Management-System-Project-In-PHP-Source-Code.zip

# Description
All login pages have a universal password vulnerability.

Poc
---
password=test&username=admin'#

# Analysis
Note: Utilizing the condition that a corresponding user name exists in the database,
in the php/functions.php file, the "$username" is not filtered, resulting in the ability to comment out the password query by using "admin'#", thereby bypassing the verification.

<img width="1452" alt="image" src="https://github.com/user-attachments/assets/95c9009b-3bb2-4d10-9b9a-d668bb85beb1">
