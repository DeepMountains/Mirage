# Vendor
flute-cms.com

# Product
Web-based CMS for server games written on PHP

# version
v0.2.2.4-alpha

# Description
By logging in as an admin user and navigating to the /admin/pages/list page, an attacker can customize routes and pages. In the page content definition, it suggests that we can insert HTML code, but even if PHP code is inserted, it will still be parsed.
<img width="1065" alt="image" src="https://github.com/user-attachments/assets/33064112-7b75-4a3f-89a6-820f21e3a2ce">

# Analysis
1. By capturing packets, it can be observed that the content of the page is sent to the server in JSON format using the PUT method. Analyzing the "app/Core/Admin/Http/Controllers/Views/PagesView.php" file also reveals the action of decoding JSON data.
<img width="1077" alt="image" src="https://github.com/user-attachments/assets/72f2aabe-94b2-42c9-9887-dcc55c17beac">

2. The vulnerability lies in the fact that PHP code must be written within an HTML object; otherwise, special characters will be escaped.
<img width="1612" alt="image" src="https://github.com/user-attachments/assets/40cb57fd-377c-4f8c-8dfb-013e5e26eb86">
<img width="1663" alt="image" src="https://github.com/user-attachments/assets/60a348bb-d6cf-4816-8b8e-a52b37f455a1">

# Step
1. Log in to the admin backend, visit the "admin/pages/list" page, and click Add.
2. Set up the route and title.
<img width="865" alt="image" src="https://github.com/user-attachments/assets/7e83aed8-0af6-4b29-acf3-e8f51551729e">
3. Add a RAW HTML object, write PHP code inside it, and then save it.
<img width="674" alt="image" src="https://github.com/user-attachments/assets/ff188c78-67d0-41a1-94fb-c3f129359d6d">
<img width="752" alt="image" src="https://github.com/user-attachments/assets/5a9e1e7e-17fb-4615-aff0-2cf4f91d33c6">
4. Visit the route you created to execute the PHP code.
<img width="826" alt="image" src="https://github.com/user-attachments/assets/2c19d2fb-7393-41fd-a40d-98f256395bc9">
