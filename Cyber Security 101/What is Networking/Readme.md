# [What is Networking?](https://tryhackme.com/room/whatisnetworking)

---

## Task 1 — What is Networking?
Networks are simply things connected. In computing, a network can be from 2 devices to billions (phones, laptops, cameras, even farms). Networking is essential to cybersecurity because it’s embedded in daily life.

**Question:** What is the key term for devices that are connected together?  
**Answer:** `network`

---

## Task 2 — What is the Internet?
The Internet is one massive network made of smaller ones (private + public).  
- Origin: **ARPANET** in the late 1960s.  
- WWW invented in **1989** by **Tim Berners-Lee**.  

**Question:** Who invented the World Wide Web?  
**Answer:** `Tim Berners-Lee`

---

## Task 3 — Identifying Devices on a Network
Devices use two identifiers:  
- **IP Address** (Internet Protocol) → changeable “name”.  
- **MAC Address** (Media Access Control) → unique “fingerprint”.  

- IPv4 = 32-bit, 4 octets (~4.29B addresses).  
- IPv6 = 128-bit, trillions of addresses.  
- Public IP = Internet-facing, Private IP = local use.  
- MAC = 12-character hex, unique but can be spoofed.  

**Question:** What does the term "IP" stand for?  
**Answer:** `Internet Protocol`  

**Question:** What is each section of an IP address called?  
**Answer:** `Octet`  

**Question:** How many sections (in digits) does an IPv4 address have?  
**Answer:** `4`  

**Question:** What does the term "MAC" stand for?  
**Answer:** `Media Access Control`  

**Question (Flag):** Deploy the lab and spoof your MAC address to access the site. What is the flag?  
**Answer:** `THM{YOU_GOT_ON_TRYHACKME}`  
**How I got it:** Changed Bob’s MAC address to Alice’s in the lab and gained access.

---

## Task 4 — Ping (ICMP)
Ping uses **ICMP** (Internet Control Message Protocol) packets to check connectivity with `echo request` and `echo reply`.  
Syntax: `ping <IP/URL>`.  

**Question:** What protocol does ping use?  
**Answer:** `ICMP`  

**Question:** What is the syntax to ping 10.10.10.10?  
**Answer:** `ping 10.10.10.10`  

**Question (Flag):** What flag do you get when you ping 8.8.8.8?  
**Answer:** `Fla{g_:THM{I_PIN_GED_TH}}`  
**How I got it:** Entered `8.8.8.8` in the ping input box on the lab site and received the flag.

---
