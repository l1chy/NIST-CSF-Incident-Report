# 🛡️ Network Incident Analysis & Hardening (Using the NIST CSF to respond to a security incident)

![Security Framework](https://img.shields.io/badge/Framework-NIST%20CSF-blue?style=flat-square)
![Focus](https://img.shields.io/badge/Focus-Incident%20Response%20%26%20Hardening-red?style=flat-square)
![Protocol](https://img.shields.io/badge/Protocol-ICMP%20%7C%20Firewall%20%7C%20IDS%2FIPS-green?style=flat-square)

## Scenario:
You are a cybersecurity analyst working for a multimedia company that offers web design services, graphic design, and social media marketing solutions to small businesses. Your organization recently experienced a DoS attack, which compromised the internal network for two hours until it was resolved.

During the attack, your organization’s network services suddenly stopped responding due to an incoming flood of ICMP packets. Normal internal network traffic could not access any network resources. The incident management team responded by blocking incoming ICMP packets, stopping all non-critical network services offline, and restoring critical network services. 

The company’s cybersecurity team then investigated the security event. They found that a malicious actor had sent a flood of ICMP pings into the company’s network through an unconfigured firewall. This vulnerability allowed the malicious attacker to overwhelm the company’s network through a denial of service (DoS) attack. 

To address this security event, the network security team implemented: 

- A new firewall rule to limit the rate of incoming ICMP packets.

- Source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets.

- Network monitoring software to detect abnormal traffic patterns.

- An IDS/IPS system to filter out some ICMP traffic based on suspicious characteristics.

---

## Incident Overview & Root Cause Analysis
* **Attack Type:** Denial of Service (DoS) — ICMP Flood
* **Vector:** Unconfigured / permissive perimeter firewall rule sets
* **Impact:** 2-hour internal network outage; starvation of internal bandwidth and resource availability
* **Resolution:** Perimeter ICMP blocking, service triage, deployment of rate-limiting filters, and IDS/IPS signature deployment

---

## 💡 Key Lessons & Takeaways
* Perimeter firewalls must always operate on a default-deny policy with strict rate limiting.
* Relying solely on basic packet filtering is insufficient; combining stateful firewalls, anti-spoofing verification, and inline IDS/IPS significantly improves and minimizes the attack surface.

---

## 📄 Project Documentation
*  **Full Technical Report (PDF):** [View Incident Report Document](./report/Incident_Report_Analysis.pdf)
