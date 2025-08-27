# Vulnerability Assessment and Penetration Testing (VAPT) — Sample Project

This repository contains a sanitized VAPT project summary, I completed as part of my cybersecurity learning journey.  
The engagement was conducted in a controlled, educational environment with explicit permission.  

---

## 🔹 Executive Summary
A vulnerability assessment and penetration test was conducted to evaluate the security exposure of a web application.  
The assessment revealed several legacy and high-risk services (FTP, Telnet, SMB, etc.), as well as evidence of the MS17-010 (EternalBlue)  vulnerability.  
Although exploitation attempts were unsuccessful (likely patched or access restricted), the presence of outdated services highlights the risk of exploitation in real-world environments.  

---

## 🔹 Scope
- Target: External web application (educational lab)  
- Test Type: Black-Box Penetration Test  
- Tools Used: Nmap, Metasploit, Wireshark  
- Date: June 2025  

---

## 🔹 Methodology
1. Reconnaissance (Nmap)  – Scanned target to identify open ports and services.  
2. Vulnerability Scanning (Metasploit) – Checked for EternalBlue (MS17-010).  
3. Exploitation Attempts – Attempted to exploit SMB, but authentication/patches blocked access.  

---

## 🔹 Key Findings

| Port  | Service    | Risk Level | Notes |
|-------|------------|------------|-------|
| 21    | FTP        | High       | Unencrypted login possible |
| 23    | Telnet     | High       | Deprecated, plaintext credentials |
| 135-139 | SMB/NetBIOS | High    | Common ransomware attack vector |
| 512-515 | Legacy UNIX services | Medium | Outdated protocols, vulnerable to abuse |
| —     | MS17-010   | Critical   | EternalBlue vulnerability detected, exploit attempt failed |


---

## 🔹 Recommendations
- Disable legacy services (Telnet, Echo, Finger, Discard).  
- Restrict SMB access from external networks.  
- Replace insecure protocols (FTP, POP3) with encrypted alternatives.  
- Apply security patches, especially MS17-010.  
- Enforce firewall rules to limit exposed services.  
- Conduct regular vulnerability scans and penetration testing.  


## 🔹 Disclaimer
This project is for **educational purposes only**.  
No unauthorized systems were tested, and all sensitive details have been removed.  


