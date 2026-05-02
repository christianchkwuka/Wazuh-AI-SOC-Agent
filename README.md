Wazuh AI SOC Agent
(SIEM-Based Threat Detection & Incident Response Lab)
🇩🇪 Projektbeschreibung (Deutsch)

Dieses Projekt demonstriert den Aufbau einer realistischen SOC-Umgebung (Security Operations Center) unter Verwendung von Wazuh SIEM, Kali Linux und einem selbst entwickelten Python-basierten AI-Agenten.

Ziel ist es, Sicherheitsvorfälle automatisch zu erkennen, zu analysieren und in Form von strukturierten Incident Reports zu dokumentieren.

🇬🇧 Project Description (English)

This project demonstrates the implementation of a realistic SOC (Security Operations Center) environment using Wazuh SIEM, Kali Linux, and a custom-built Python-based AI agent.

The goal is to automatically detect, analyze, and document security incidents in structured incident reports.

🔧 Verwendete Technologien / Technologies Used
Wazuh SIEM
Kali Linux (Attack Simulation)
Windows Server 2022 (Target System)
Python (Automation & AI Agent)
MITRE ATT&CK Framework
GitHub (Documentation & Version Control)
⚙️ Lab-Architektur / Lab Architecture
Ubuntu Server → Wazuh Manager
Windows Server → Target System
Kali Linux → Attack Simulation
Python Agent → Alert Analysis & Reporting
🚨 Beispiel-Szenario / Example Scenario
Durchführung eines Port-Scans mit Nmap (Kali Linux)
Erkennung durch Wazuh SIEM
Klassifizierung des Events durch den AI-Agenten
Erstellung eines Incident Reports mit MITRE ATT&CK Mapping
📊 Ergebnisse / Results
Automatische Erkennung von Sicherheitsereignissen
Klassifizierung nach Schweregrad (LOW → CRITICAL)
MITRE ATT&CK Mapping (z. B. T1110 – Brute Force)
Generierung von Incident Reports
Export von Audit-Evidence (CSV)
📁 Projektstruktur / Project Structure
agent/          → Python SOC Agent  
reports/        → Generated Incident Reports  
evidence/       → CSV Audit Logs  
docs/           → Documentation  
screenshots/    → Proof of Implementation  
🎯 Ziel / Objective

Dieses Projekt simuliert reale SOC-Prozesse und dient als Nachweis praktischer Kenntnisse in:

SIEM Monitoring
Incident Response
Threat Detection
GRC & Compliance (ISO 27001 / NIST)
👨‍💻 Autor / Author

Christian Chukwuka
Cybersecurity & IT Audit Enthusiast
