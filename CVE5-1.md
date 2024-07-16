# Vendor
flute-cms.com

# Product
Web-based CMS for server games written on PHP

# version
v0.2.2.4-alpha

# Description
By registering an account and logging in, you can upload PHP files on the avatar upload page, but it requires modifying the header information of the PHP file to bypass detection.

# Analysis
1. In the app/Core/Http/Controllers/Profile/ImagesController.php file, it can be observed that this controller's image validation is based on the type rather than the file extension.
<img width="1109" alt="image" src="https://github.com/user-attachments/assets/ea0b81e6-5a74-4f34-a9ad-c5b6296ed613">

2. The allowed file types are shown in the profile.php file.
<img width="806" alt="image" src="https://github.com/user-attachments/assets/3b324f7c-76d4-4372-a343-ab544e3efc51">

# Step
Register a user and log in, modify the user avatar, upload a PHP file, and add the header GIF89a.
<img width="933" alt="image" src="https://github.com/user-attachments/assets/32f0ebed-efe4-4ebd-bff4-1f2ea73bb069">

<img width="1212" alt="image" src="https://github.com/user-attachments/assets/39a1da14-4b8a-474d-b92e-e2b6e5ccb2b5">

