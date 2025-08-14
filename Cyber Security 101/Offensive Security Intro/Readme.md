# [TryHackMe – Cyber Security 101: Offensive Security Intro](https://tryhackme.com/room/offensivesecurityintro?path=cybersecurity101)

## Overview

*"To outsmart a hacker, you need to think like one."*

Offensive Security is the practice of simulating attacks on systems to find vulnerabilities before malicious hackers can exploit them. This includes breaking into systems, exploiting software bugs, and identifying weaknesses in applications to strengthen defenses.

In this TryHackMe room, you’ll hack your first website in a **legal and safe environment** to understand how ethical hackers operate.

---

## Task 1 – What is Offensive Security?

### Key Concept:

* Offensive Security = Thinking like a hacker to find vulnerabilities.
* Defensive Security = Protecting systems from attacks.

**Question:**
Which of the following options better represents the process where you simulate a hacker's actions to find vulnerabilities in a system?

**Answer:**

```
Offensive Security
```

---

## Task 2 – Hacking Your First Machine

### Virtual Machines:

TryHackMe uses Virtual Machines (VMs) to create safe, simulated environments for hands-on practice.

### Target:

* FakeBank: A simulated banking application.

### Steps:

#### 1. Start the Machine

Click **Start Machine**. Use **Show Split View** to see both instructions and the machine side-by-side.

#### 2. Open the Terminal

* Terminal = command-line interface to interact with the machine.
* Click the **Terminal icon** on the right.

#### 3. Use Gobuster to Find Hidden Pages

**Command:**

```bash
gobuster -u http://fakebank.thm -w wordlist.txt dir
```

**Explanation:**

* `-u` specifies the URL to scan.
* `-w` specifies the wordlist of potential directories/pages.
* Gobuster will show pages that exist (Status: 200).

**Example Output:**

```
/images (Status: 301)
/bank-transfer (Status: 200)
```

#### 4. Access the Hidden Page

* Navigate to `/bank-transfer` in the browser.
* This page simulates admin-level access to transfer money.
* **Mission:** Transfer \$2000 from account **2276** to your account **8881**.

**Confirmation:**

* Check your new account balance.
* Message above balance:

```
BANK-HACKED
```

---

## Task 3 – Careers in Cyber Security

### Getting Started:

* Break down your learning.
* Pick an area of cyber security that interests you.
* Practice daily on TryHackMe for hands-on experience.

### Career Examples:

* **Penetration Tester:** Finds exploitable vulnerabilities in systems.
* **Red Teamer:** Simulates attacks from an adversary’s perspective.
* **Security Engineer:** Designs, monitors, and maintains security controls to prevent attacks.

No answer needed to complete this task.

---

**Notes:**

* All exercises are **legal and safe**.
* Focus on learning methods, not just the answers.
* Keep practicing; small, consistent progress builds expertise.

---
