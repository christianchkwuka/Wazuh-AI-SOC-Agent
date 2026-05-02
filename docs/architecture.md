# 🏗️ Architektur der SOC-Umgebung

# 🏗️ SOC Architecture

---

## 🇩🇪 Überblick

Diese Lab-Umgebung simuliert ein reales Unternehmensnetzwerk mit integrierter Sicherheitsüberwachung (SOC).

Die Architektur kombiniert Angriffssimulation, Netzwerküberwachung, SIEM-Analyse und automatisierte Incident-Response.

---

## 🇬🇧 Overview

This lab environment simulates a real enterprise network with integrated security monitoring (SOC).

The architecture combines attack simulation, network monitoring, SIEM analysis, and automated incident response.

---

## 🖥️ Komponenten / Components

| System         | Rolle (Deutsch)                   | Role (English)                |
| -------------- | --------------------------------- | ----------------------------- |
| Kali Linux     | Angriffssystem                    | Attack machine                |
| pfSense        | Firewall & Netzwerküberwachung    | Firewall & Network monitoring |
| Windows Server | Zielsystem                        | Target system                 |
| Ubuntu Server  | Wazuh SIEM (Manager, Indexer, UI) | Wazuh SIEM (Manager, Indexer) |
| Python Agent   | Analyse & Reporting               | Analysis & Reporting          |

---

## 🔄 Datenfluss / Data Flow

1. Kali Linux führt einen Angriff aus (z. B. Nmap Scan)
2. Der Traffic läuft durch die pfSense Firewall
3. pfSense protokolliert und überwacht den Traffic
4. Logs werden an Wazuh weitergeleitet
5. Wazuh erkennt das Sicherheitsereignis
6. Alerts werden in `alerts.json` gespeichert
7. Python-Agent liest und analysiert die Logs
8. Incident Report wird generiert

---

## 🌐 Netzwerkstruktur / Network Structure

```id="net1"
Kali Linux (Attacker)
        ↓
pfSense Firewall
        ↓
Windows Server (Target)
        ↓
Wazuh SIEM (Ubuntu)
        ↓
Python AI Agent
        ↓
Incident Reports / Evidence
```

---

## 🛡️ Sicherheitsfunktionen / Security Features

* Firewall-Regeln (Allow / Deny)
* Netzwerküberwachung durch pfSense
* IDS/IPS (optional mit Suricata)
* Zentrale Log-Erfassung durch Wazuh
* Automatische Analyse durch Python-Agent
* Incident Reporting (Markdown + CSV)

---

## 🚨 Beispiel-Angriff / Example Attack

* Port Scan (Nmap) von Kali Linux
* Erkennung durch Wazuh SIEM
* Klassifizierung als potenzieller Angriff
* Zuordnung zu MITRE ATT&CK
* Generierung eines Incident Reports

---

## 🎯 Ziel der Architektur / Architecture Objective

Ziel ist die Simulation eines realistischen SOC-Workflows:

* Detection (Wazuh SIEM)
* Analysis (Python Agent)
* Response (Empfohlene Maßnahmen)
* Documentation (Reports & Evidence)

---

## 📌 Hinweis / Note

Diese Architektur ist modular aufgebaut und kann erweitert werden, z. B. durch:

* Automatische Blockierung von Angreifern (pfSense API)
* Erweiterte Korrelation von Logs
* Dashboard-Visualisierung (z. B. Streamlit)

