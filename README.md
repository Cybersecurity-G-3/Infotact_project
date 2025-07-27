🔐 DVWA Vulnerability Assessment

This project is a hands-on penetration testing exercise conducted using Damn Vulnerable Web Application (DVWA) to explore and exploit the OWASP Top 10 vulnerabilities. It aims to simulate real-world attacks and understand exploitat techniques, their impact, and recommended remediations.

📌 Project Objectives

Identify and exploit common web application vulnerabilities.

Use tools like Burp Suite, Sqlmap, and Kali Linux.

Document the vulnerabilities with payloads and remediation strategies.

Strengthen understanding of offensive and defensive web security techniques.

🛠️ Tools Used

Kali Linux

DVWA (Damn Vulnerable Web Application)

Burp Suite

Sqlmap

FoxyProxy

Metasploit wordlists

Browser Developer Tools

⚙️ Setup Instructions

Install Kali Linux in a VM (e.g., VMware or VirtualBox).

Install and configure DVWA on localhost.

Open DVWA in the browser: http://localhost/dvwa

Set security level as needed from the DVWA security settings.

Launch tools (Burp Suite, Sqlmap, etc.) and begin assessments.

🔍 Vulnerabilities Explored

1. SQL Injection (SQLi)
Injected payloads to bypass authentication and extract data.

Tools used: Burp Suite, Sqlmap

✅ Extracted usernames and passwords from the database.

2. Cross-Site Scripting (XSS)
Explored all types: Reflected, Stored, DOM-based

Payload used: <script>alert('xss')</script>

Observed behavior at low, medium, and high security levels.

3. Broken Access Control
Uploaded a PHP shell (shell.php) as a low-privilege user.

Gained code execution and revealed server identity (www-data).

4. Broken Authentication (Brute Force)
Used Burp Intruder with Metasploit wordlists.

Identified valid credentials based on response length.

5. Sensitive Data Exposure
Observed plaintext credentials and session tokens.

Inspected cookies and insecure HTTP communications.

6. Security Misconfiguration
Enabled directory listing exposed sensitive files

Remediation: Disable listing with Options -Indexes in Apache config.

📋 OWASP Top 10 Mapped

Vulnerability	Demonstrated
Broken Access Control	✅
Cryptographic Failures (Sensitive Data Exposure)	✅
Injection (SQLi, Command)	✅
Insecure Design	⚠️ Covered partially
Security Misconfiguration	✅
Vulnerable and Outdated Components	⚠️ (DVWA setup)
Identification & Authentication Failures	✅
Software and Data Integrity Failures	⚠️ Not demonstrated
Security Logging and Monitoring Failures	⚠️ Not monitored
Server-Side Request Forgery (SSRF)	❌ Not tested

🧠 Key Learnings

Gained hands-on experience in offensive security.

Understood attacker mindset and exploitation patterns.

Learned how security controls change behavior across different levels.

Developed defensive strategies and secure coding recommendations.

✅ Conclusion

This project provided a complete walkthrough of how attackers exploit real-world vulnerabilities and how developers/security professionals can mitigate them. By working through each vulnerability in DVWA, I enhanced my practical skills in penetration testing, web security, and ethical hacking.

