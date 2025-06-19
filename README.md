# Project Change Healthcare Feb 2024

# TITLE : *Change Healthcare Ransomware Attack Analysis (Feb 2024) with MITRE ATT&CK Mapping*
---- 
## OBJECTIVE :
    
  To analyze the February 2024 ransomware attack on Change Healthcare (a subsidiary of UnitedHealth Group) by the BlackCat (ALPHV) group, mapping the attacker behavior to the MITRE ATT&CK framework and demonstrating   how a SOC analyst would approach detecting and understanding this real-world incident.

1. Attack Overview
In February 2024, Change Healthcare suffered a ransomware attack that significantly disrupted U.S. healthcare operations. The attacker, a known Ransomware-as-a-Service (RaaS) group called BlackCat (ALPHV), used stolen credentials to infiltrate the network, deploy ransomware, and exfiltrate sensitive healthcare data including PHI and PII. The breach affected hospitals, pharmacies, and insurance workflows nationwide.

Threat Actor: BlackCat (aka ALPHV)Attack Type: Ransomware (RaaS model)Impact: Service disruption, data exfiltration, operational outages across U.S. healthcare services

2. 2. Data Compromised

PHI (Protected Health Information): Treatment histories, prescriptions, billing records

PII (Personally Identifiable Information): Names, addresses, SSNs, insurance IDs

These data types are regulated under HIPAA and their exposure can result in legal, financial, and reputational damage.

3. MITRE ATT&CK Mapping
   | Tactic | Technique | Technique ID | Description |
   |----    |  -----    |    -------   | -----       |
   | Initial Access | Valid Accounts | T1078 | Used stolen Citrix credentials for access |
   | Execution | Command and Scripting Interpreter | T1059 | PowerShell or batch scripts to execute payloads |
   | Persistence |  Create or Modify System Process | T1543 | Created malicious services to maintain access|
   | Privilege Escalation | Exploitation for Privilege Escalation | T1068 | Exploited system vulnerabilities
