# MITRE ATT&CK Mapping – APT31 Case Study

[📄 Download Full Project Report](./Group5_WK10_MITRELab_11072025.docx)

---

## Overview
This project analyzes the APT31 cyber espionage campaign targeting the Czech Ministry of Foreign Affairs.  
I mapped the attacker’s behaviors to MITRE ATT&CK techniques based on public threat intelligence and reporting.

---

## MITRE ATT&CK Heatmap

**Screenshot:**  
![MITRE Heatmap](https://i.imgur.com/XAF7PyQ.png)

(Upload your heatmap to Imgur or GitHub, then paste the link above.)

---

## Key Techniques Identified

**Initial Access**
- Spearphishing Attachment (T1566.001)  
- Exploit Public-Facing Application (T1190)  

**Execution**
- Command & Scripting Interpreter (T1059)  
- Scheduled Task (T1053.005)  

**Persistence**
- DLL Side-Loading (T1574.002)  
- Scheduled Task (T1053.005)  

**Privilege Escalation**
- Exploitation for Privilege Escalation (T1068)

**Defense Evasion**
- System Binary Proxy Execution (T1218)  
- Obfuscated/Encrypted Files (T1027)

**Credential Access**
- OS Credential Dumping (T1003)

**Lateral Movement**
- Remote Desktop Protocol (T1021.001)

**Command & Control**
- Application Layer Protocol – HTTPS (T1071.001)

---

## Case Summary
APT31 exploited two SharePoint vulnerabilities (CVE-2025-49706 & CVE-2025-49704) to deploy the ToolShell post-exploitation framework and maintain long-term access.  
The operation resulted in multi-year espionage inside Czech government networks.

---

## Detection & Defense Recommendations
- Enable MFA for all remote and privileged accounts  
- Monitor scheduled tasks (Event IDs 4698–4702)  
- Enable PowerShell Script Block Logging  
- Watch for encoded PowerShell (“-EncodedCommand”)  
- Detect DLL side-loading in non-standard paths  
- Monitor outbound HTTPS traffic to new / rare domains  
- Follow Zero Trust principles and segment sensitive networks  

---

## Files Included
- **Word report:** Full analysis  
- **MITRE heatmap image**  
