# Task-1: Scan Your Local Network for Open Ports

**Objective:**  
Learn to discover open ports on devices in your local network to understand network exposure and potential vulnerabilities.

---

## 🧰 Tools Used

- [Nmap](https://nmap.org/download.html) – for network scanning
- [Wireshark (optional)](https://www.wireshark.org/download.html) – for packet analysis

---

## 📝 Task Steps

### ✅ Step 1: Install Nmap

- Download from: [https://nmap.org/download.html](https://nmap.org/download.html)
- **Linux Installation:**
  ```bash
  sudo apt install nmap

✅ Step 2: Find Your Local IP Range

  Linux/Mac:
    Run ifconfig or ip a

  Example:
    If your IP is 192.168.1.10 and subnet is 255.255.255.0, your network range is 192.168.1.0/24

✅ Step 3: Run Nmap TCP SYN Scan

  nmap -sS 192.168.1.0/24
    -sS = TCP SYN scan (fast and stealthy)

  To save results in text format:
    nmap -sS 192.168.1.0/24 -oN scan_results.txt

✅ Step 4: Analyze the Output
Review discovered:
  IP addresses
  Open ports
  Services (e.g., HTTP, SSH)

✅ Step 5: Research Common Services
  Port	Service	Risk
  21	  FTP	    ⚠️ Insecure (unencrypted)
  22	  SSH	    ✅ Secure if properly configured
  23	  Telnet	❌ Deprecated and insecure
  80	  HTTP	  ⚠️ Unencrypted web service
  443	  HTTPS	  ✅ Secure web service
