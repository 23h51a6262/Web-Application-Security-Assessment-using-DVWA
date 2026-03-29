# Web Application Security Assessment using DVWA

## Overview

This project demonstrates a **Vulnerability Assessment and Penetration Testing (VAPT)** exercise performed on a deliberately vulnerable web application (**DVWA**) hosted on **Metasploitable 2**.

The objective is to identify, exploit, and analyze common web application vulnerabilities in a controlled lab environment using industry-standard tools and techniques.

---

## Objectives

* Identify and exploit SQL Injection vulnerabilities
* Demonstrate Cross-Site Scripting (XSS) attacks
* Perform Command Injection and privilege checks
* Conduct network reconnaissance using Nmap
* Perform web vulnerability scanning using Nikto

---

## Tools and Technologies

* Kali Linux
* Metasploitable 2
* DVWA (Damn Vulnerable Web Application)
* Nmap
* Nikto
* Oracle VirtualBox

---

## Lab Environment

* **Attacker Machine:** Kali Linux
* **Target Machine:** Metasploitable 2
* **Network Configuration:** Host-Only Network

---

## Methodology

### 1. Reconnaissance

* Identified target IP address using system network tools
* Performed port and service scanning using:

  ```bash
  nmap -A <target-ip>
  ```

### 2. Application Access

* Accessed DVWA through web browser
* Configured security level to low for testing

### 3. Exploitation

#### SQL Injection

* Performed UNION-based SQL Injection
* Extracted database information including tables and credentials

#### Cross-Site Scripting (XSS)

* Executed reflected and stored XSS payloads
* Verified client-side script execution

#### Command Injection

* Executed system commands via input fields
* Verified execution context and privileges

### 4. Vulnerability Scanning

* Performed web server scanning using:

  ```bash
  nikto -h http://<target-ip>
  ```

---

## Results

* Successfully identified and exploited SQL Injection vulnerability
* Retrieved database information and user credentials
* Demonstrated execution of malicious scripts via XSS
* Achieved command execution on the target system
* Identified insecure configurations and exposed services

---

## OWASP Top 10 Mapping

* SQL Injection → A03: Injection
* Cross-Site Scripting (XSS) → A03: Injection
* Command Injection → A03: Injection
* Security Misconfiguration → A05: Security Misconfiguration

---

## Skills Demonstrated

* Web Application Penetration Testing
* Vulnerability Assessment (VAPT)
* SQL Injection Exploitation
* Cross-Site Scripting (XSS)
* Command Injection
* Network Reconnaissance (Nmap)
* Web Vulnerability Scanning (Nikto)

---

## Screenshots

> Screenshots of the lab setup and attack execution are available in the `/screenshots` directory.

---

## How to Reproduce

1. Install Oracle VirtualBox
2. Set up Kali Linux and Metasploitable 2 virtual machines
3. Configure Host-Only network between machines
4. Start both machines
5. Identify target IP using:

   ```bash
   ifconfig
   ```
6. Access DVWA:

   ```
   http://<target-ip>/dvwa
   ```
7. Login credentials:

   * Username: admin
   * Password: password

---

## Project Structure

```
/screenshots/
   (attack screenshots)

/report/
   VAPT_Report.pdf

README.md
```

---

## Future Work

* Extend testing to full OWASP Top 10 coverage
* Integrate automated scanning tools
* Add remediation techniques with secure code examples
* Integrate findings with SIEM platforms (Splunk/ELK)

---

## Author

Y.Pragnavi
Cybersecurity Student

---
