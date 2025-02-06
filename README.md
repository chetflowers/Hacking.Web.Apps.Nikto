# Exploiting Web Vulnerabilities in DVWA with Nikto: A Lab Demonstration of SQL Injection, XSS, & Command Injection

## Quick Links
- [Overview](#overview)
- [Detailed Google Slides](#detailed-google-slides)
- [Environment Setup](#environment-setup)
- [Vulnerabilities Exploited](#vulnerabilities-exploited)
- [Tools and Technologies](#tools-and-technologies)
- [Exploitation Process](#exploitation-process)
- [Mitigation Strategies](#mitigation-strategies)
- [Conclusion](#conclusion)

## Overview
This project focuses on exploiting common web vulnerabilities such as SQL Injection (SQLi), Cross-Site Scripting (XSS), and Command Injection using the Nikto web server scanner in a secure Kali Linux environment. The testing is performed in a controlled virtual environment using the Damn Vulnerable Web Application (DVWA) to simulate real-world attack scenarios. The project is part of a broader cybersecurity exercise designed to showcase offensive security techniques while discussing mitigation strategies.

## Objective
The primary goal is to demonstrate how Nikto can be utilized to identify and exploit web vulnerabilities. The project highlights:
- The importance of a secure, isolated testing environment.
- Practical steps for exploiting vulnerabilities like SQLi, XSS, and Command Injection.
- Best practices for remediation, including input validation, parameterized queries, and the principle of least privilege.

## Detailed Google Slides
I’ve prepared a **comprehensive slideshow** detailing the Nikto exploitation steps, including screenshots and an in-depth walkthrough.  
- **[View the Detailed Presentation](https://chetflowers.github.io/Hacking.Web.Apps.Nikto/)**  
  (Visit our GitHub Pages site for an embedded slideshow and complete documentation.)

## Environment Setup
- **Kali Linux:** Used as the primary platform for running Nikto and other security tools.
- **DVWA:** Configured for vulnerability testing, simulating a real-world vulnerable web application.
- **Virtual Environment:** Ensures all tests and scans are conducted securely, preventing unintended impact on actual systems.

## Vulnerabilities Exploited
1. **SQL Injection (SQLi):** Demonstrated using manual exploitation techniques and automated tools like SQLMap to extract sensitive data from databases.
2. **Cross-Site Scripting (XSS):** Exploited to capture session cookies and perform actions on behalf of other users.
3. **Command Injection:** Demonstrated how attackers can execute arbitrary commands on the server, potentially leading to full system compromise.

## Tools and Technologies
- **Nikto:** Utilized for vulnerability scanning and identifying exploitable points in the DVWA setup.
- **SQLMap:** Automated tool for exploiting SQL Injection vulnerabilities.
- **Apache Web Server & PHP:** Hosting the attack scripts and logging captured data.
- **Kali Linux:** Central hub for managing the testing environment and running the tools.
- **Virtual Machines:** Isolated setup with Kali and DVWA running in a secure network for controlled testing.

## Exploitation Process
- **SQL Injection (SQLi):** Exploiting the vulnerability to dump sensitive information like usernames and password hashes.
- **XSS (Reflected):** Injecting malicious scripts to capture cookies and hijack sessions.
- **Command Injection:** Executing arbitrary system commands through vulnerable input fields in DVWA.

## Mitigation Strategies
- **Input Validation and Output Encoding:** Ensuring all user inputs are sanitized and properly encoded before rendering.
- **Use of `HttpOnly` Flag:** Protecting session cookies from being accessed via JavaScript.
- **Parameterized Queries:** Preventing SQL Injection by using prepared statements.
- **Content Security Policy (CSP):** Implementing CSP headers to limit script sources and reduce XSS risks.
- **Least Privilege:** Restricting database and server access to the minimum necessary for functionality.

## Conclusion
This project demonstrates the significance of understanding both the offensive and defensive sides of cybersecurity. By simulating real-world attacks, it highlights the critical vulnerabilities that attackers can exploit and offers actionable remediation strategies. The controlled environment ensures safe testing and provides an in-depth exploration of the attack surface while reinforcing the importance of continuous security assessments.
