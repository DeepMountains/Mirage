# Description

In the website design page functionality, Cross-site scripting(xss) vulnerabilities can be exploited in multiple locations

# Step
1. Log in as the admin user.
2. Visit the page "/index.php?module=admin&act=dispMenuAdminSiteDesign".
3. Select "Layout" -> "Default Layout" -> "Setting" : Malicious script code can be written in the positions of "Website Footer Text" and "Head Script"
<img width="1556" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/938236b7-646c-4571-ae01-0f3f2c1a61d6">
<img width="1316" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/e0720e90-00c9-4334-8e41-db7ffe401596">

5. Save change
<img width="1565" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/ff5b74e6-400a-4e56-a860-0d90bd6e8083">

6. Select "Layout" -> "Default Layout" -> "HTML/CSS" -> Modify layout.html ,Inserting script code can also achieve injection
7. Refresh Home Page,Trigger script code

<img width="1060" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/f82e32e2-3525-4c1f-8615-8594531947c0">
<img width="1099" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/c41a9e49-4117-4623-82ed-de61714ccbbe">

