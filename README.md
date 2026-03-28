# 🔐 VAPT Lab – Web Application Security Assessment (DVWA)

Overview

This project demonstrates a Vulnerability Assessment and Penetration Testing (VAPT) lab conducted on a deliberately vulnerable web application (DVWA) hosted on Metasploitable 2.

The objective is to identify, exploit, and analyze common web vulnerabilities in a controlled environment.

## 🎯 Objectives

* Identify SQL Injection vulnerabilities
* Perform UNION-based SQL Injection attacks
* Exploit Command Injection for privilege escalation
* Demonstrate Cross-Site Scripting (XSS)
* Perform network scanning and vulnerability assessment

---

## 🛠️ Tools Used

* Kali Linux
* Metasploitable 2
* DVWA (Damn Vulnerable Web Application)
* Nmap
* Nikto
* VirtualBox

---

## 🧪 Lab Setup

* Attacker Machine: Kali Linux
* Target Machine: Metasploitable 2
* Network: Host-Only Adapter

---

## 🔍 Key Experiments

### 1. Network Scanning

```bash
nmap -A 192.168.56.101
```

### 2. SQL Injection (UNION Based)

```sql
1' UNION SELECT user, password FROM users#
```

### 3. Command Injection

```bash
127.0.0.1; whoami
```

### 4. Cross-Site Scripting (XSS)

```html
<script>alert('XSS')</script>
```

### 5. Vulnerability Scanning

```bash
nikto -h http://192.168.56.101
```

---

## 📊 Results

* Extracted database information via SQL Injection
* Achieved remote command execution
* Demonstrated stored and reflected XSS
* Identified misconfigured services

---

## 🛡️ Security Recommendations

* Use prepared statements
* Validate and sanitize input
* Disable unnecessary services
* Apply regular security patches
* Use Web Application Firewalls

---

## 📸 Screenshots

* Nmap scan results
* SQL Injection output
* XSS alert
* Command execution

---

## 📚 Learning Outcomes

* Hands-on penetration testing
* Understanding real-world vulnerabilities
* Practical use of security tools
* Attack methodology and mitigation

---
 Author

Y.Pragnavi
Cybersecurity Student 

---
