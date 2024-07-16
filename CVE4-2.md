# Description
In the wuhu system, the pages.php page contains custom template statements defined by wuhu. Through source code analysis, it can be found that the {{EVAL:}} method can directly achieve local file inclusion. However, there are no restrictions on the path of the included page, which can lead to arbitrary file inclusion vulnerabilities through directory traversal.

# Version
2024

# Analysis
1. /www_admin/pages: In the pages.php section of the system, custom template statements are stored in the intranet_minuswiki_pages table of the database.
<img width="511" alt="image" src="https://github.com/user-attachments/assets/180e6f5e-a24a-4097-9cf4-95f3c13b6ed1">


2. /www_party/minuswiki.inc.php:
