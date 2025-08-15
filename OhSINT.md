# TryHackMe – OSINT Challenge Walkthrough

## Overview

This room focuses on **Open-Source Intelligence (OSINT)** — collecting and analyzing information from publicly available sources such as social media, websites, and online tools.
You’ll work with an image file to uncover hidden details, pivot across platforms, and answer seven questions.

---

## **Task Preparation**

1. **Download Task Files**

   * Click the **Download Task Files** button in Task 1.
   * File: `WindowsXP.jpg`

2. **Initial Inspection**

   * Viewing image properties directly gives no useful info.

---

## **Step 1 – Extract Metadata with ExifTool**

**Tool:** [ExifTool by Phil Harvey](https://exiftool.org/)

1. Download the **Windows executable**.
2. Extract it into a folder (keep `WindowsXP.jpg` in the same folder).
3. Rename the application to `exiftool.exe`.
4. Open terminal in this folder:

   * **Shift + Right Click** → **Open in Terminal**
5. Run:

   ```cmd
   exiftool.exe WindowsXP.jpg
   ```
6. From the output, note:

   * Copyright info
   * GPS coordinates
   * Username: `OWoodflint`

---

## **Step 2 – Find Social Media Accounts**

1. Google search:

   ```
   OWoodflint
   ```
2. Results found:

   * Twitter
   * GitHub
   * WordPress blog

---

## **Q1 – What is this user’s avatar of?**

* Check **Twitter profile** → Avatar is a **cat**.
  **Answer:** `cat`

---

## **Q2 – What city is this person in?**

1. On **Twitter**, find a post mentioning:

   ```
   Bssid: B4:5D:50:AA:86:41
   ```
2. Go to [wigle.net](https://wigle.net/) → **Advanced Search**.
3. Enter the **BSSID** in *Network Characteristics* and query.
4. Map link shows location → **London**.

**Answer:** `London`

---

## **Q3 – What’s the SSID of the WAP he connected to?**

* Found in Wigle.net search results for the same BSSID.
  **Answer:** `UnileverWiFi`

---

## **Q4 – What is his personal email address?**

1. Visit **GitHub page**: [github.com/OWoodfl1nt/people\_finder](https://github.com/OWoodfl1nt/people_finder)
2. Email listed:

   ```
   OWoodflint@gmail.com
   ```

**Answer:** `OWoodflint@gmail.com`

---

## **Q5 – What site did you find his email address on?**

**Answer:** `GitHub`

---

## **Q6 – Where has he gone on holiday?**

1. Visit **WordPress blog**: [oliverwoodflint.wordpress.com/author/owoodflint/](https://oliverwoodflint.wordpress.com/author/owoodflint/)
2. Blog post mentions **holiday in New York**.

**Answer:** `New York`

---

## **Q7 – What is this person’s password?**

1. On the **WordPress blog**, open **page source** (`Ctrl+U`) or select all text (`Ctrl+A`).
2. White-colored hidden text is revealed as the password.

**Answer:** *(password found in hidden text)*

---

## **Final Answers Summary**

| # | Question               | Answer                                              |
| - | ---------------------- | --------------------------------------------------- |
| 1 | User’s avatar          | cat                                                 |
| 2 | City                   | London                                              |
| 3 | SSID                   | UnileverWiFi                                        |
| 4 | Personal email         | [OWoodflint@gmail.com](mailto:OWoodflint@gmail.com) |
| 5 | Site where email found | GitHub                                              |
| 6 | Holiday location       | New York                                            |
| 7 | Password               | *(hidden text in blog source)*                      |

---

## **Key Tools Used**

* [ExifTool](https://exiftool.org/) – Extract image metadata
* [wigle.net](https://wigle.net/) – BSSID to location lookup
* Google Search – Username enumeration
* GitHub – Public repo analysis
* WordPress – Content & source inspection

---
