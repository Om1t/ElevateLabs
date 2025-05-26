Task 1: Port Scanning with Nmap

The goal of this task was to perform a TCP SYN scan on my local network to discover live hosts and open ports. This helps understand the exposure of networked devices and learn the basics of network reconnaissance.

---

## 🛠 Tools Used
- **Nmap** (Version 7.93)
- Linux terminal (for IP address discovery)

---

 Step 1: Find Local IP Address

### Command:

ip addr show

---

Step 2: Run Nmap TCP SYN Scan

sudo nmap -sS 192.168.71.131/24

---

| IP Address     | Status | Open/Filtered Ports | Details                          |
| -------------- | ------ | ------------------- | -------------------------------- |
| 192.168.71.2   | Up     | 53/tcp (filtered)   | DNS service, possibly firewalled |
| 192.168.71.254 | Up     | All ports filtered  | Likely a gateway or firewall     |
| 192.168.71.131 | Up     | All ports closed    | My machine, no active services   |

---

Observations & Security Analysis
Filtered ports indicate firewall presence or packet filtering, which is a good security practice.

Port 53 (DNS) being filtered shows it is protected, but if misconfigured, it could be vulnerable to attacks like DNS spoofing or amplification.

No obviously open ports were detected, which is a sign of a secure network.

---

Outcome

Understood how to identify live devices on a local network.

Learned to use Nmap for TCP SYN scanning.

Analyzed scan results to assess potential security risks.

---

Files Included

Task1.txt: Raw terminal output from the IP and Nmap scan.
