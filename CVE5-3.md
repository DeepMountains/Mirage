# Vendor

flute-cms.com

# Product

Web-based CMS for server games written on PHP

# version

v0.2.2.4-alpha
Download Source Code: https://github.com/Flute-CMS/cms

# Description
In the creation of "Notifications," the website has predefined four templates for the notification content: {name}, {login}, {email}, and {balance}. However, upon analyzing the PHP code, it is revealed that inserting other template injection statements into the content can still be executed, for example, {system("whoami")}.

# Analysis
1. Upon examining the app/Core/Support/ContentParser.php file, it can be found that the replaceContent() function takes the input Content string and passes it to replaceUserContent() for processing, resulting in the output corresponding to {name}, {login}, {email}, and {balance}.
<img width="1054" alt="image" src="https://github.com/user-attachments/assets/bfc90b0d-1c2a-4bed-b9f5-aa3bcf4cad3d">
<img width="883" alt="image" src="https://github.com/user-attachments/assets/41e784a2-edce-4c8f-91ab-5dfc85942e14">

2. However, after returning the string, it doesn't stop there. The replaceContent() function continues to check for the existence of {}, extracts the content within {}, and passes the matched content to the evaluateExpression() function for processing.
<img width="1057" alt="image" src="https://github.com/user-attachments/assets/f2f81338-f040-42d4-8013-6741bf08c17d">

3. As a result, matches[1] will be used as the method name, and matches[2] will serve as the parameters passed in, resulting in the execution of a command.
<img width="870" alt="image" src="https://github.com/user-attachments/assets/62354a2c-6c5b-4e6f-85a6-15947e377f63">

# step
1. Log in with an admin user.

2. Click on the notification function to create a new notification. Set the notification message trigger event to "User Login" and write the POC "{system("ls")}" in the Content field.
<img width="1279" alt="image" src="https://github.com/user-attachments/assets/e34e2b00-c41f-4943-9fab-f5f9450e41a8">

3. Log back in with the admin user or create a new user account to log in. The results of the command execution can be obtained on the notification page.
<img width="513" alt="image" src="https://github.com/user-attachments/assets/37367213-b911-40fa-8d2d-c71c892f55ec">


