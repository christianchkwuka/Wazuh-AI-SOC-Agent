# 🚨 Incident Response Prozess

# 🚨 Incident Response Process

---

## 🇩🇪 Ziel

Dieser Prozess beschreibt, wie Sicherheitsvorfälle im SOC erkannt, analysiert und behandelt werden.

Er basiert auf Best Practices und orientiert sich an Standards wie **ISO 27001** und **NIST Incident Response Framework**.

---

## 🇬🇧 Objective

This process describes how security incidents are detected, analyzed, and handled within the SOC.

It follows best practices aligned with **ISO 27001** and the **NIST Incident Response Framework**.

---

## 🔄 Phasen des Incident Response / Incident Response Phases

### 1️⃣ Erkennung (Detection)

* Wazuh SIEM überwacht kontinuierlich Logs
* Alerts werden basierend auf Regeln generiert
* Beispiele:

  * Failed Logins
  * Port Scans
  * Suspicious Network Activity

---

### 2️⃣ Analyse (Analysis)

* Python AI Agent liest `alerts.json`
* Klassifizierung des Events nach:

  * Severity (LOW → CRITICAL)
  * Event-Typ
* Zuordnung zu **MITRE ATT&CK Techniken**

---

### 3️⃣ Bewertung (Classification)

* Einschätzung des Risikos
* Identifikation:

  * Quelle (Source IP)
  * Zielsystem (Agent)
  * Häufigkeit des Events

---

### 4️⃣ Reaktion (Response)

Empfohlene Maßnahmen:

* Überprüfung der Wazuh Logs
* Analyse der Source IP
* Verifikation des betroffenen Systems
* Identifikation wiederholter Angriffe
* Optional: Blockierung über pfSense Firewall

---

### 5️⃣ Dokumentation (Reporting)

* Erstellung eines Incident Reports (.md)
* Export von Evidence (CSV)
* Speicherung für Audit- und Compliance-Zwecke

---

## 🌐 Incident Workflow (Visual)

```id="flow1"
Attack → Detection → Analysis → Classification → Response → Reporting
```

---

## 🚨 Beispiel: Brute-Force Angriff

* **Event:** Mehrere fehlgeschlagene Login-Versuche
* **Detection:** Wazuh Alert (Rule Level 9)
* **MITRE ATT&CK:** T1110 – Brute Force
* **Severity:** HIGH

---

## 📊 Beispiel Incident Report Inhalte

* Timestamp
* Agent Name / IP
* Source IP
* Rule ID / Level
* MITRE ATT&CK Mapping
* Beschreibung des Vorfalls
* Empfohlene Maßnahmen

---

## 🛡️ Bezug zu Standards / Compliance Mapping

* **ISO 27001**

  * A.12 Logging & Monitoring
  * A.16 Incident Management

* **NIST**

  * Detection
  * Analysis
  * Containment
  * Recovery

---

## 🎯 Ziel / Outcome

* Strukturierte Incident-Behandlung
* Schnelle Reaktion auf Bedrohungen
* Nachvollziehbare Dokumentation
* Unterstützung von Audits und Compliance

---

## 📌 Hinweis / Note

Dieser Prozess kann erweitert werden durch:

* Automatische Reaktion (z. B. IP Blocking via pfSense API)
* Integration von Threat Intelligence
* Erweiterte Korrelation von Logs
