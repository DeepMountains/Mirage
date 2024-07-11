# Description
In the website design page functionality, SSTi injection can be achieved by modifying layout.html:

# Step

1. Log in as the admin user.
2. Visit the page "/index.php?module=admin&act=dispMenuAdminSiteDesign".
3. Select "Layout" -> "Default Layout" -> "HTML/CSS" -> Modify layout.html.
4. Insert the POC "{system('ls')}" at any location with template code.
5. Save the layout.html template, then save the website design settings.
6. Refresh Home Page,view source code,View the content of command execution.

<img width="1460" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/bd8077b1-e5ca-4c17-826c-26d99eaf8642">

<img width="1024" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/dc334811-e6a8-417e-a18f-02e8bb15626f">
