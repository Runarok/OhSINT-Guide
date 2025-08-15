# [TryHackMe – Cyber Security 101: Defensive Security Intro](https://tryhackme.com/room/defensivesecurityintro?path=cybersecurity101)

## Overview

*"The best attack is the one you stop before it begins."*

Defensive Security is the practice of preparing for, preventing, and responding to cyber threats. Known as the **blue team**, defensive security focuses on monitoring, detection, and mitigation to protect systems from malicious actors.

In this TryHackMe room, you’ll explore defensive security concepts, see how SOC teams operate, and practice using a SIEM to investigate suspicious activity.

---

## Task 1 – Introduction to Defensive Security

### Key Concepts:

* **Defensive Security (Blue Team)** = Protecting systems from intrusions and minimising impact when they occur.
* Two primary objectives:

  1. **Prevent intrusions** through proactive measures.
  2. **Detect and respond** to threats when they happen.

**Common Activities:**

* **Cyber Security Awareness** — Training users about phishing, social engineering, etc.
* **Documenting & Managing Assets** — Knowing all systems to protect them.
* **Preventative Security** — Firewalls, IPS, etc., to control and block malicious traffic.
* **Logging & Monitoring** — Recording network/system activity to detect threats.
* **Frameworks, Policies & Procedures** — Creating security policies for proper device use.

**Question:**
Which team focuses on defensive security?

**Answer:**

```
Blue team
```

---

## Task 2 – Exploring the SOC

### Key Concepts:

* **Security Operations Centre (SOC)** = A team of cyber security professionals monitoring systems for malicious activity.

**SOC Responsibilities:**

* **Trends & Vulnerability Awareness:** Stay updated on latest threats.
* **Policy Violations:** Detect when security rules are broken.
* **Unauthorised & Illegal Activity:** Investigate abnormal behaviour.
* **Intrusion & Breach Detection:** Identify and respond to attacks.

**Question:**
What would you call a team of cyber security professionals that monitors a network and its systems for malicious events?

**Answer:**

```
Security Operations Centre
```

---

## Task 3 – Digital Forensics

### Key Concepts:

* Digital forensics applies investigative techniques to digital devices to preserve and analyse evidence during an incident.

**Data Sources:**

* **File System:** Analyse installed programs, deleted files, and activity history.
* **System Memory:** Identify malicious programs running in memory but not saved to disk.
* **System Logs:** Review event histories for suspicious behaviour.
* **Network Logs:** Inspect traffic data for attack indicators.

**Scenario:**
An attacker runs malicious code entirely in memory, never writing it to disk.

**Question:**
What digital forensics technique would we use in this instance?

**Answer:**

```
System Memory
```

---

## Task 4 – Incident Response

### Key Concepts:

* Incident Response = A structured process for handling security incidents to minimise damage and recover quickly.

**Stages:**

1. **Preparation:** Build teams, tools, and training (including cyber awareness).
2. **Detection & Analysis:** Identify and assess the scope of incidents.
3. **Containment, Eradication, and Recovery:** Limit spread, remove threats, restore systems.
4. **Post-Incident Activity:** Review, learn, and improve processes.

**Question:**
What phase of the incident response process involves providing "cyber awareness" training to employees?

**Answer:**

```
Preparation
```

---

## **Task 5 – Practical Example of Defensive Security**

### **Key Concepts**

* **Security Information and Event Management (SIEM)** tools collect, aggregate, and analyse security logs from various sources.
* These tools generate alerts for suspicious activities and help Security Operations Center (SOC) analysts investigate potential incidents.
* SOC analysts use SIEM dashboards to track anomalies, investigate alerts, escalate incidents, and take defensive actions like blocking malicious IPs.

---

### **Exercise – Simulation Walkthrough**

You’ll simulate the role of a SOC analyst by investigating a suspicious alert in a simplified SIEM dashboard.

**Steps:**

1. **Access the SIEM Dashboard**
   Open the simulation environment to view incoming alerts.

2. **Identify the Highlighted Alert**
   Out of the five alerts displayed, only one “Alert Log” is highlighted in **red**, indicating high severity.

3. **Copy the Malicious IP Address**
   From the red-highlighted alert, note the suspicious IP:

   ```
   143.110.250.149
   ```

4. **Investigate the IP Address**
   Paste this IP into open-source threat intelligence tools like:

   * **AbuseIPDB**
   * **Cisco Talos Intelligence**
     These platforms provide reputation scores, geolocation, and known malicious activity history.
     Analysts often use such databases to confirm whether an IP is safe or compromised.

5. **Verify and Confirm**
   The tools confirm the IP is malicious. This matches the alert’s warning in the SIEM.

6. **Escalate the Incident**
   Select the responsible SOC team member to escalate the issue to. {Will Griffin – SOC Team Lead}

7. **Block the Malicious IP**
   Add the IP address to your firewall’s block list to prevent further traffic from this source.

8. **Flag Appears**
   Once blocked, the SIEM confirms with the flag.

### **Flag Obtained**

```
THREAT-BLOCKED
```

---
