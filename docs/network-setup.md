# Network Setup

## Overview

The experiment was conducted in an **isolated offline laboratory environment** designed to simulate a realistic enterprise network. The environment consisted of two separate networks:

* **Attacker Network** – used to simulate an external adversary.
* **Target Network** – contained the defensive infrastructure and victim machines.

All attacks originated from the attacker network and were forced to traverse the defensive layers of the target network.

---

## Network Architecture

The target network included multiple security layers designed to simulate a real-world enterprise environment.

Components included:

* pfSense firewall
* Suricata IDS/IPS
* Distributed switch with VLAN segmentation
* Endpoint security software
* Windows client machines
* Microsoft Exchange mail server

<img width="4652" height="2612" alt="network-diagram (1)" src="https://github.com/user-attachments/assets/cea46e36-d5f4-465d-99ba-d40db8d37194" />

---

## VLAN Segmentation

The network was segmented into four VLANs to enforce access control and limit lateral movement.

### Trusted VLAN

Used by internal employees and trusted systems. This VLAN had access to the internet and other internal services.

### DMZ VLAN

Hosts exposed services such as the email server. Access was restricted to only necessary ports.

### Guest VLAN

Provided internet access for guest devices while preventing access to internal network resources.

### Management VLAN

Reserved for administrative access to network infrastructure devices.

Segmentation was implemented to restrict lateral movement in the event of a compromise.

---

## Firewall and Network Monitoring

### pfSense Firewall

The pfSense firewall enforced strict access control rules that blocked all traffic except necessary services such as:

* RDP
* Email services

### Suricata IDS/IPS

Suricata was deployed as an intrusion detection and prevention system. It monitored network traffic in real time and detected malicious activity using:

* signature detection
* behavioral analysis
* threat intelligence feeds

---

## Endpoint Security

The baseline setup used:

* Microsoft Defender

The multilayered security configurations included combinations of:

* Avast Premium Security
* Bitdefender
* ZoneAlarm
* Comodo Firewall
* Malwarebytes

These tools provided multiple layers of protection including antivirus, firewall protection, and behavioral monitoring.
