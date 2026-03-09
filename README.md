# Ransomware-defense-lab
This project simulates a ransomware attack against a small enterprise environment built using Active Directory and Windows infrastructure.  The goal of the lab was to analyze ransomware attack techniques and evaluate the effectiveness of multilayered defense mechanisms including firewalls, endpoint protection, and SIEM monitoring.

The experiment focused on three main areas:
- detection effectiveness
- response and deletion time
- containment of ransomware propagation

## Lab Architecture
The lab was built as an offline environment consisting of:
- attacker network
- target network
- Windows endpoints
- Active Directory
- Microsoft Exchange server
- pfSense firewall
- Suricata IDS/IPS
- VLAN segmentation
- Wazuh SIEM

![Network Diagram](images/network-diagram.png)

## Attack Scenarios
The following attack scenarios were tested:
- drive-by download and malvertising
- phishing email delivery
- RDP brute-force and credential-based access

## Security Layers Evaluated
Baseline setup:
- Windows Defender

Multilayered configurations:
- pfSense
- Suricata
- VLAN segmentation
- Avast
- Bitdefender
- ZoneAlarm
- Comodo Firewall
- Malwarebytes

## Monitoring and Analysis
Security events were monitored using:
- Wazuh SIEM
- Windows Event Viewer
- Wireshark
- Procmon

## Key Findings
- Baseline security detected some ransomware samples, but several bypassed detection and successfully encrypted systems.
- Multilayered defense consistently improved detection and prevention across all tested scenarios.
- Network segmentation limited ransomware lateral movement and prevented propagation across VLANs.
- Suricata provided valuable network-level detection of malicious traffic and brute-force activity.
- Behavioral and layered detection significantly reduced the impact of ransomware execution.

## Results Summary
### Detection Effectiveness
Multilayered defense detected all tested ransomware samples across the evaluated scenarios, while the baseline setup failed to detect several samples.

### Detection and Deletion Speed
Several multilayered tools detected and removed threats significantly faster than the baseline configuration.

### Containment
Ransomware samples attempted internal reconnaissance and SMB-based lateral movement, but segmentation and endpoint controls limited spread.

## Skills Demonstrated
- Active Directory administration
- SIEM monitoring with Wazuh
- Windows log analysis
- Network traffic analysis
- Ransomware simulation
- IDS/IPS monitoring with Suricata
- VLAN segmentation and network security architecture
- Detection engineering and incident analysis


## Disclaimer
This project was conducted in a controlled lab environment for academic and educational purposes only.
