# Key Findings

## Baseline Security Limitations

The baseline configuration relying on Windows Defender was capable of detecting some ransomware samples but failed to detect several others.

Some ransomware samples successfully executed and encrypted the system after bypassing detection.

This demonstrates the limitations of relying on a single security layer.

---

## Benefits of Multilayered Defense

The multilayered defense significantly improved detection and prevention across all tested attack scenarios.

Key improvements included:

* faster threat detection
* better containment
* improved visibility into network activity

Using multiple defensive technologies created overlapping layers of protection that reduced the likelihood of successful attacks.

---

## Importance of Network Segmentation

VLAN segmentation prevented ransomware from spreading across the network.

Although ransomware attempted to enumerate devices within the local VLAN, communication across VLAN boundaries was blocked.

This greatly limited the potential impact of the attack.

---

## Detection Beyond Signatures

Several security tools relied on behavioral detection rather than signature-based detection.

Behavioral analysis proved effective at identifying ransomware even when the malware was previously unknown.

This highlights the importance of combining signature-based detection with behavior-based monitoring.

---

## Human Factors

The experiment also highlighted the role of user behavior in security.

Several attack scenarios relied on user interaction such as:

* downloading suspicious files
* opening malicious attachments

User awareness and training remain essential components of a comprehensive defense strategy.
