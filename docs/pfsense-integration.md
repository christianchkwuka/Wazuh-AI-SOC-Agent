# pfSense Integration mit Wazuh SIEM

## Ziel
Integration der pfSense Firewall in das Wazuh SIEM zur Überwachung von Netzwerkverkehr und Sicherheitsereignissen.

## Architektur
pfSense → Syslog → Wazuh Manager → SIEM Dashboard → AI Agent

## Konfiguration

### pfSense
- Remote Logging aktiviert
- Ziel: 192.168.56.103:514
- Log-Typen:
  - Firewall Events
  - System Logs

### Wazuh
- Syslog Empfang aktiviert (UDP 514)
- Logs werden im Archiv gespeichert

## Test
- Durchführung eines Nmap-Scans
- Erkennung von Port-Scan Aktivitäten

## Ergebnis
- Logs erfolgreich empfangen
- Ereignisse im Wazuh Dashboard sichtbar
- Incident Reports automatisch generiert

## Mehrwert
- Realistische Simulation eines SOC
- Netzwerküberwachung + Angriffserkennung
