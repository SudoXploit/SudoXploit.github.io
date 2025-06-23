# 🔐 DVWA SQL Injection – Login Bypass (Web App Pentest Lab)

A hands-on security lab showcasing **SQL Injection authentication bypass** against [DVWA (Damn Vulnerable Web Application)](https://github.com/digininja/DVWA) running on a local XAMPP stack. This project demonstrates how classic SQLi techniques can be leveraged to gain unauthorized access to a web app's admin panel, complete with Burp Suite interception and payload crafting.

> ✅ Designed for educational and ethical testing purposes only.

---

## 📌 Project Overview

This lab simulates a real-world web application vulnerability using DVWA's *Low Security* configuration. The objective is to:

- Perform authentication bypass using SQL Injection payloads
- Understand the underlying SQL logic being exploited
- Practice with Burp Suite, MySQL, and XAMPP in a controlled environment

It’s part of a broader pentesting portfolio exploring various attack vectors in lab environments.

---

## ⚙️ Tools & Technologies Used

| Tool / Technology      | Purpose                                |
|------------------------|----------------------------------------|
| **XAMPP (Apache + MySQL)** | Local hosting of DVWA instance        |
| **DVWA**               | Vulnerable PHP web application         |
| **MySQL**              | Backend database for DVWA              |
| **Burp Suite Community** | Proxy/interception of HTTP requests  |
| **Firefox**            | Browser for accessing localhost        |
| **PHP**                | Server-side logic                      |

---

## 🛠️ Installation & Prerequisites

### 1. Requirements

- OS: Windows 10/11, Linux, or macOS
- [XAMPP](https://www.apachefriends.org/) installed and configured
- [DVWA GitHub Repo](https://github.com/digininja/DVWA) cloned into `htdocs/`
- PHP enabled and `config.inc.php` properly set

### 2. Database Setup

Launch **phpMyAdmin** or use the MySQL CLI and ensure the following:

```sql
CREATE DATABASE dvwa;
CREATE USER 'dvwa'@'localhost' IDENTIFIED BY 'p@ssw0rd';
GRANT ALL PRIVILEGES ON dvwa.* TO 'dvwa'@'localhost';
FLUSH PRIVILEGES;
