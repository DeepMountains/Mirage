# Description
In the wuhu system, the pages.php page contains custom template statements defined by wuhu. Through source code analysis, it can be found that the {{EVAL:}} method can directly achieve local file inclusion. However, there are no restrictions on the path of the included page, which can lead to arbitrary file inclusion vulnerabilities through directory traversal.

# Version
2024

# Analysis
1. /www_admin/pages: In the pages.php section of the system, custom template statements are stored in the intranet_minuswiki_pages table of the database.
<img width="511" alt="image" src="https://github.com/user-attachments/assets/180e6f5e-a24a-4097-9cf4-95f3c13b6ed1">

2. /www_party/minuswiki.inc.php: In the syntax shown below, extract the content within {{}}. If the content before the ":" matches eval, include the corresponding file after the ":". It can be seen that there are no strict restrictions on the path.
<img width="1068" alt="image" src="https://github.com/user-attachments/assets/b4717e88-38e6-4911-ab67-6c3765bf5b0f">
<img width="938" alt="image" src="https://github.com/user-attachments/assets/4fa25000-02ce-41ac-9ab2-1943ef0cda5c">

# Step
1. Visit the /pages.php?edit=News page and write the PoC "{{Eval:../../../../../../../etc/passwd}}".
<img width="704" alt="image" src="https://github.com/user-attachments/assets/73577bf6-9325-462a-ae88-e9f2abcc50d8">

2. Visit the /www_party/index.php?page=News page to trigger the file inclusion.
<img width="982" alt="image" src="https://github.com/user-attachments/assets/d0851e1a-2488-4bd8-9c70-678217c08875">
