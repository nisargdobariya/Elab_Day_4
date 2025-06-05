# 🔐 CYBER SECURITY INTERNSHIP – TASK 4  
## 🧱 Firewall Configuration Using UFW (Tasks 1 – 6)

This README documents every step and screenshot for Tasks 1 to 6 of the internship’s firewall exercise using **UFW (Uncomplicated Firewall)** on Ubuntu Linux.

---

### 🔹 Task 1 – Open Firewall Configuration Tool, Install & Enable UFW

**Commands**
```bash
sudo apt update
sudo apt install ufw -y
sudo ufw enable
```
![Task 1 Screenshot](/1.png)

---

### 🔹 Task 2 – List Current Firewall Rules

**Command**
```bash
sudo ufw status numbered
```
![Task 2 Screenshot](/2.png)

---

### 🔹 Task 3 – Block Inbound Traffic on Port 23 (Telnet)

**Command**
```bash
sudo ufw deny 23
```

![Task 3 Screenshot](/3.png)

---

### 🔹 Task 4 – Test the Rule by Connecting to Port 23

**Commands**
```bash
sudo apt install telnet -y        # install telnet if missing
telnet localhost 23               # expect "Connection refused"
```

![Task 4 Screenshot](/4.png)

---

### 🔹 Task 5 – Allow SSH on Port 22

**Command**
```bash
sudo ufw allow 22
```

![Task 5 Screenshot](/5.png)

---

### 🔹 Task 6 – Remove the Telnet Block Rule (Restore State)

**Command**
```bash
sudo ufw delete deny 23
```

![Task 6 Screenshot](/6.png)

---

### 🔹 Task 8 – Summarize How Firewall Filters Traffic

**Description:**  
In this task, we summarize the function of a firewall and how it manages network traffic.

**Summary:**  
A firewall is a security system that controls incoming and outgoing traffic based on predetermined security rules. It helps protect systems from unauthorized access while allowing legitimate communication to pass through.

In our previous tasks:

- We **blocked port 23 (Telnet)** to prevent insecure remote connections.
- We **allowed port 22 (SSH)** to maintain secure remote access.
- We tested firewall behavior using tools like `telnet`.
- We reverted temporary rules to restore system state.

Firewalls can be **stateful** (track connection states) or **stateless** (filter based on simple rules).  
UFW simplifies complex firewall configurations with easy-to-use commands.

By using UFW:
- We reduced the attack surface.
- We enforced principle of least privilege.
- We gained visibility and control over allowed services.

This task reinforced how important firewall rule design is in securing modern systems.

## ✅ Summary

By following these six tasks we have:

* Installed and enabled **UFW**.
* Reviewed existing firewall rules.
* Blocked insecure Telnet traffic on port 23.
* Verified the block with a Telnet connection test.
* Allowed secure SSH traffic on port 22.
* Cleaned up by removing the temporary Telnet block.

These steps show how firewalls filter traffic to reduce the attack surface while maintaining necessary remote‑management access.
