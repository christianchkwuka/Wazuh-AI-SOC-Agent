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


# pfSense Integration with Wazuh SIEM

## Objective
Integrate pfSense firewall logs into Wazuh SIEM for monitoring network activity and detecting security threats.

## Architecture
pfSense → Syslog → Wazuh Manager → SIEM Dashboard → AI Agent

## Configuration

### pfSense
- Remote logging enabled
- Destination: 192.168.56.103:514
- Log types:
  - Firewall events
  - System logs

### Wazuh
- Syslog input configured (UDP 514)
- Logs stored in archive

## Testing
- Performed Nmap scan from Kali Linux
- Detected port scanning activity

## Results
- Logs successfully ingested
- Events visible in Wazuh dashboard
- Incident reports generated automatically

## Value
- Real-world SOC simulation
- Network monitoring and threat detection
