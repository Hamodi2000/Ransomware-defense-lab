# Attack Scenarios

The experiment simulated several common ransomware attack vectors observed in real-world incidents.

---

# Drive-By Download and Malvertising

In this scenario, users visited a malicious website hosted on the attacker network.

Two attack methods were tested:

* **Drive-by download:** ransomware automatically downloaded when the user visited the webpage.
* **Malvertising:** ransomware downloaded when the user clicked a malicious advertisement.

This scenario tested the effectiveness of:

* browser security features
* endpoint antivirus detection
* network intrusion prevention systems.

---

# Phishing Email

Phishing emails containing ransomware payloads were sent to victim machines.

Emails were delivered using:

* Proton Mail
* Tuta Mail

The victim machines received emails through:

* Gmail
* Outlook
* Microsoft Exchange server

Attachments included:

* executable files
* ZIP archives
* password-protected ZIP files

This scenario evaluated the effectiveness of email filtering and endpoint detection.

---

# RDP Brute Force Attack

The attacker attempted to gain access to the target system using brute-force login attempts against Remote Desktop Protocol (RDP).

The Hydra tool was used to automate credential guessing.

Example command:

```
hydra -L users.txt -P passwords.txt rdp://10.0.10.23:3389
```

This scenario evaluated:

* account lockout policies
* endpoint firewall protection
* intrusion detection systems.

---

# Credential-Based RDP Access

In a second RDP scenario, the attacker used valid credentials obtained through credential theft.

Once authenticated, the attacker was able to:

* disable security software
* download ransomware
* execute ransomware payloads

This scenario demonstrated the importance of post-authentication defenses.
