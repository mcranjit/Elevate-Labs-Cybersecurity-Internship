**Task 1 (Local Network Port Scan using Nmap)**:

---

````markdown
# 🔍 Local Network Port Scanner using Nmap

This project performs a comprehensive scan of a local network target to identify open ports, running services, and potential security risks using the Nmap tool. It is part of a cybersecurity learning task aimed at understanding network exposure.

---

## 📌 Objective

To discover open ports on a local network host, identify services, and assess potential vulnerabilities.

---

## 🛠 Tools Used

- **Nmap** – Network Mapper
- **xsltproc** – For converting XML output to readable HTML
- **Kali Linux** – Operating system used for scanning

---

## 🧪 Scan Configuration

**Target IP:** `192.168.152.129`  
**Command Used:**
```bash
sudo nmap -v -sV -A -p1-65535 192.168.152.129 -oX port.xml
xsltproc port.xml -o port.html````

### 🔍 Scan Options Explanation:

| Flag        | Description                                      |
| ----------- | ------------------------------------------------ |
| `-v`        | Verbose mode                                     |
| `-sV`       | Service/version detection                        |
| `-A`        | Enables OS detection, version, script scan, etc. |
| `-p1-65535` | Scan all TCP ports                               |
| `-oX`       | Save output in XML format                        |

---

## 📄 Results Summary

| Port | Service   | Version/Product                | Risk Level  |
| ---- | --------- | ------------------------------ | ----------- |
| 21   | FTP       | vsftpd 2.3.4 (anonymous login) | 🔴 High     |
| 22   | SSH       | OpenSSH 4.7p1 (Debian)         | 🟡 Medium   |
| 23   | Telnet    | Linux telnetd                  | 🔴 High     |
| 80   | HTTP      | Apache 2.2.8 (Ubuntu)          | 🟡 Medium   |
| 3306 | MySQL     | MySQL 5.0.51a                  | 🟡 Medium   |
| 1524 | Bindshell | Metasploitable Root Shell      | 🔴 Critical |
| …    | …         | …                              | …           |

> 📝 See full report in `port.html` for complete list of 30+ open ports.

---

## ⚠️ Security Observations

* Anonymous FTP login is allowed.
* Telnet is open (plaintext credentials).
* Multiple outdated services (Apache, SSH, MySQL).
* Presence of a remote root shell (intentional in Metasploitable).
* Databases exposed to the network.

---

## 📂 Files Included

| File        | Description                            |
| ----------- | -------------------------------------- |
| `port.xml`  | Raw Nmap scan output in XML format     |
| `port.html` | Beautiful HTML scan report (converted) |
| `README.md` | This project documentation             |

---

## 🚀 How to Run

1. Install Nmap and xsltproc (Kali has them by default).
2. Replace `192.168.152.129` with your target's IP.
3. Run the command:

   ```bash
   sudo nmap -v -sV -A -p1-65535 <target_ip> -oX port.xml
   xsltproc port.xml -o port.html
   ```
4. Open `port.html` in your browser to view results.

---

📄 Report Output
🔗 [**Click here to view the live Nmap HTML Report**](https://ranjith241.neocities.org/port)

---

## 🧠 Learning Outcome

This task builds practical skills in:

* Network discovery
* Port and service enumeration
* Identifying outdated/insecure services
* Reporting scan results in professional formats

---

## 📜 License

This project is for educational purposes only. Do **not** scan any system without **explicit authorization**.

---
