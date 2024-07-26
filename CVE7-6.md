# Vendor

itsourcecode

# Product

Society Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2021/04/Society-Management-System-Project-In-PHP-Free-Download-Source-Code.zip

# Description

After logging into the website backend, on the /admin/student.php page, it is possible to create student accounts and upload account avatars. The vulnerability lies in the fact that the uploaded avatar file is not strictly filtered, allowing PHP files to be uploaded.
<img width="1079" alt="image" src="https://github.com/user-attachments/assets/11f61822-befc-48eb-aa23-53c7e77a16e8">

# Step
1. On the /admin/admin.php page, use an SQL injection vulnerability to log into the website backend with a universal password.
2. On the /admin/student.php page, create a user and upload a webshell file in the avatar upload section.
   
<img width="1301" alt="image" src="https://github.com/user-attachments/assets/5efeb70d-bdc2-48a5-852e-7d7e60d0d0ae">
<img width="1324" alt="image" src="https://github.com/user-attachments/assets/c8feb1ad-1548-4459-9f0d-023421378bbe">

3. Access the webshell at: /upload/shell.php.

<img width="716" alt="image" src="https://github.com/user-attachments/assets/2a6a99aa-80c9-4ade-bfc1-a6fb03a3cca9">
