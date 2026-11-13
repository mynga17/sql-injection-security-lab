![SQL](https://img.shields.io/badge/SQL-Database-blue)
![Apache](https://img.shields.io/badge/Apache-Web_Server-red)
![ModSecurity](https://img.shields.io/badge/ModSecurity-WAF-orange)
![OWASP CRS](https://img.shields.io/badge/OWASP-CRS-black)
![VMware](https://img.shields.io/badge/VMware-Lab-607078)

# 🛡️ SQL Injection Security Lab

A practical cybersecurity lab focused on understanding, exploiting, and mitigating SQL Injection vulnerabilities in a controlled virtualized environment.

The project demonstrates SQL Injection attacks and explores defensive techniques using Prepared Statements and ModSecurity with OWASP Core Rule Set (CRS) on Apache.

---
## Table of Contents

- [Overview](#overview)
- [Project Objectives](#project-objectives)
- [Vulnerability Background](#vulnerability-background)
- [Lab Environment](#lab-environment)
- [Attack Demonstration](#attack-demonstration)
- [Mitigation and Prevention](#mitigation-and-prevention)
- [Video Demonstrations](#video-demonstrations)
- [Documentation](#documentation)
- [Disclaimer](#disclaimer)
---
<a id="overview"></a>
## 📌 Overview

SQL Injection is a web application vulnerability that occurs when untrusted user input is improperly incorporated into SQL queries. It can potentially allow attackers to manipulate database operations and access unauthorized information.

This project was developed as part of my Information Security studies to gain practical experience in web application security testing and vulnerability mitigation.

The lab covers two main activities:

- **Attack Demonstration:** Exploring SQL Injection vulnerabilities and their potential impact.
- **Mitigation Demonstration:** Applying defensive measures to reduce SQL Injection risks.

<a id="project-objectives"></a>
## ✨ Project Objectives

- Understand the principles and security risks of SQL Injection.
- Explore how insecure user input handling affects SQL queries.
- Perform practical SQL Injection testing in an isolated lab environment.
- Implement Prepared Statements to secure database queries.
- Deploy ModSecurity with OWASP CRS on Apache as an additional security layer.
- Examine the effectiveness of the implemented defensive measures.

<a id="vulnerability-background"></a>
## 🔍 Vulnerability Background

SQL Injection occurs when user-controlled input is processed as part of a dynamically constructed SQL statement without proper protection.

Depending on the vulnerable application and database configuration, successful exploitation may allow attackers to:

- Bypass authentication mechanisms.
- Retrieve unauthorized database information.
- Manipulate database records.
- Perform other unauthorized database operations.

<a id="lab-environment"></a>
## 🖥️ Lab Environment

The experiment was conducted in a virtualized environment using VMware.

### Technologies & Tools

| Category | Technologies |
|---|---|
| Virtualization | VMware Workstation |
| Web Server | Apache |
| Web Application Security | ModSecurity |
| Security Rules | OWASP ModSecurity Core Rule Set (CRS) |
| Database Security | SQL, Prepared Statements |

*The virtual machines and complete lab environment are not included in this repository.*

<a id="attack-demonstration"></a>
## ⚔️ Attack Demonstration

The attack phase focuses on identifying and exploiting an SQL Injection vulnerability within the lab application.

The demonstration explores how improperly handled input can influence SQL query execution and illustrates the potential impact on application and database security.

<a id="mitigation-and-prevention"></a>
## 🔐 Mitigation  Prevention

Two complementary defensive approaches were implemented.

### 1. Prepared Statements

Prepared Statements were used to separate SQL query structures from user-supplied data.

By parameterizing user input, the application can treat supplied values as data rather than executable SQL syntax, significantly reducing SQL Injection risks.

### 2. ModSecurity with OWASP CRS

ModSecurity was deployed as a Web Application Firewall (WAF) on Apache, together with the OWASP ModSecurity Core Rule Set (CRS).

This configuration provides an additional layer of protection by inspecting incoming HTTP requests and applying security rules to detect and help block common web attacks, including SQL Injection attempts.

### Defense in Depth

The two approaches serve different purposes:

| Security Layer | Protection Mechanism |
|---|---|
| Application Layer | Prepared Statements |
| HTTP / WAF Layer | ModSecurity + OWASP CRS |

Using both approaches provides layered protection rather than relying on the WAF as a replacement for secure application development.

<a id="video-demonstrations"></a>
## 🎬 Video Demonstrations

The following videos document the practical attack and mitigation experiments.

### 🔴 SQL Injection Attack

Demonstrates the SQL Injection vulnerability and its potential impact in the lab environment.

**[▶ Watch Attack Demonstration](https://youtu.be/T11x6I6AGj8)**

### 🟢 SQL Injection Mitigation

Demonstrates the implementation of Prepared Statements and ModSecurity with OWASP CRS on Apache.

**[▶ Watch Mitigation Demonstration](https://youtu.be/k8MkWZNxg6c)**

<a id="documentation"></a>
## 📄 Documentation

The accompanying project report provides further details about the lab environment, vulnerability demonstration, experimental process, observations, and mitigation techniques.

- [SQL Injection Demo Report](SQL_Injection_Demo_Report.pdf)

<a id="disclaimer"></a>
## ⚠️ Disclaimer

This project was conducted in an isolated virtual lab environment for educational and cybersecurity research purposes.

All testing activities were performed on systems under the project's control. No unauthorized systems, applications, or databases were targeted.
