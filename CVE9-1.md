# Vendor

juzaweb.com

# Product

juzaweb cms

# version

v3.4.2

Download Source Code: https://github.com/juzaweb/cms/releases/tag/v3.4.2

# Description

After logging into the administrator account, an attacker can modify the website templates through the "/admin-cp/theme/editor/default" page. By utilizing the source and include functions in Twig templates, the attacker can read files. Furthermore, due to the lack of strict filtering on the input file paths, the attacker can achieve arbitrary file reading using directory traversal techniques.

# Poc

```
{{ source('../../../../../../../../../../../../../../etc/passwd') }}
```
<img width="1560" alt="image" src="https://github.com/user-attachments/assets/0f35faee-1da2-4ec3-9e20-170fad93c4fb">

# Analysis

1. Using the {{ constant('PHP_VERSION') }} syntax test, it was found that the site uses the Twig template engine. In Twig templates, executing arbitrary PHP code (including system commands) is prohibited by default.
2. After analyzing the juzaweb/modules/modules/CMS/Extension/CustomFunction.php code, it was determined that there are no methods defined in the site's custom functions that allow code execution.
<img width="1370" alt="image" src="https://github.com/user-attachments/assets/dc321814-0f86-4a11-b569-82333fcc0f92">

3. Arbitrary file reading is achieved using the source function.
<img width="788" alt="image" src="https://github.com/user-attachments/assets/76bde654-3baf-41fc-b4cc-b2e609529b3e">


