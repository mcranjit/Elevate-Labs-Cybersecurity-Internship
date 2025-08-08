🔥 Task 4: : Setup and Use a Firewall on Windows/Linux

### 🎯 Objective

Configure a firewall on Kali Linux using **UFW (Uncomplicated Firewall)** to allow and block specific ports, simulate filtered traffic, and document firewall behavior.

---

### 🛠 Environment

* **Operating System:** Kali Linux
* **Tool Used:** UFW (Uncomplicated Firewall)

---

### 🧪 Steps Performed

1. **Checked Initial Firewall Status**

```bash
sudo ufw status verbose
```

🟡 Result: `Status: inactive`

2. **Enabled UFW**

```bash
sudo ufw enable
```

✅ Result: `Firewall is active and enabled on system startup`

3. **Allowed SSH on Port 22**

```bash
sudo ufw allow 22
```

4. **Blocked Telnet on Port 23**

```bash
sudo ufw deny 23
```

5. **Verified Active Rules**

```bash
sudo ufw status numbered
```

Result:

```
[ 1] 22                         ALLOW IN    Anywhere                  
[ 2] 23                         DENY IN     Anywhere                  
[ 3] 22 (v6)                    ALLOW IN    Anywhere (v6)             
[ 4] 23 (v6)                    DENY IN     Anywhere (v6)
```

6. **Deleted Deny Rule for Port 23 (IPv4)**

```bash
sudo ufw delete 2
```

7. **Re-added Deny Rule for Port 23**

```bash
sudo ufw deny 23
```

8. **Final Check**

```bash
sudo ufw status numbered
```

Result:

```
[ 1] 22                         ALLOW IN    Anywhere                  
[ 2] 23                         DENY IN     Anywhere                  
[ 3] 22 (v6)                    ALLOW IN    Anywhere (v6)             
[ 4] 23 (v6)                    DENY IN     Anywhere (v6)
```

---

### 📸 Screenshots Included

* UFW status and rule display
* Port 23 block test
* Rule deletion and re-addition steps

---

### ✅ Outcome

* UFW successfully enabled and configured
* SSH allowed, Telnet blocked
* Rules verified using command-line
* Practiced rule deletion and restoration

---

### 🧾Documented Commands Used

Here’s a full list of all UFW commands used in this task:

Purpose	Command
Check status	sudo ufw status verbose
Enable UFW	sudo ufw enable
Allow port 22	sudo ufw allow 22
Deny port 23	sudo ufw deny 23
View numbered rules	sudo ufw status numbered
Delete a rule (e.g., #2)	sudo ufw delete 2
Re-add deny rule	sudo ufw deny 23

No GUI steps were used, as all configurations were done via terminal.

---

### 🔎How Firewall Filters Traffic

A firewall works by applying rules that either allow or block network traffic based on specific conditions such as:

Port number

IP address

Protocol (TCP/UDP)

In this task, UFW filtered traffic based on incoming port numbers:

It allowed SSH (port 22), so connections on that port were permitted.

It denied Telnet (port 23), blocking all incoming attempts on that port.

These rules act as a protective barrier, only letting trusted traffic through and dropping or rejecting anything unauthorized — effectively reducing attack surfaces and unauthorized access risks.

---
