# Task 2 — Phishing Email Analysis

This repository contains the complete analysis for **Task 2**, where a suspicious email claiming to be from Revolut was examined to determine whether it was a phishing attempt. The investigation follows a structured cybersecurity approach, including header analysis, authentication checks, routing evaluation, and body content inspection.

---

## Repository Contents

- **email.txt** — Full raw email (headers + body)
- **headers.txt** — Extracted email headers used for technical analysis
- **analysis_report.md** — Detailed phishing analysis report
- **quick_findings.txt** — Short summary of important indicators (optional)
- **screenshots/** — Supporting screenshots (optional)

---

## 🔍 What Was Analyzed

### **1. Email Headers**
- `From:` and `Return-Path:` comparison 
- Verification of sender domain authenticity 
- Inspection of `Message-ID`, `Date`, and other metadata

### **2. Routing Information (Received Headers)**
- Identification of actual sending servers 
- Detection of unusual or unknown mail relays 
- Tracing back to potential spoofed origins

### **3. Authentication Results**
Checked the following mechanisms:
- **SPF** (Sender Policy Framework)
- **DKIM** (DomainKeys Identified Mail)
- **DMARC** (Domain-based Message Authentication)

Failing any of these strongly suggests spoofing.

### **4. URL Extraction**
- Safe extraction of all URLs using text tools 
- Verification of domain legitimacy 
- Identification of phishing redirect links

### **5. Social Engineering Indicators**
Examined:
- Urgency or threats ("account suspended") 
- Impersonation of trusted brands 
- Manipulative tone or unusual requests 

---

## 🧪 Tools Used

- Linux Mint XFCE (2GB system)
- `grep`, `awk`, `sed`, `less`
- `ripgrep (rg)` (optional)
- `nano`, `gedit`
- Git + GitHub

---

## 📝 Summary of Findings

The email was confirmed to be a **phishing attempt** due to:

- **SPF = fail**, **DKIM = none**, **DMARC = fail** 
- Originating from unknown / suspicious servers 
- Sender domain not matching Revolut (`revolut-example.com`) 
- Malicious link: `http://revolut-verify.example.com/review` 
- Strong social engineering tactics urging immediate action 

---

## 🛡 Conclusion

The message is **not legitimate** and is designed to harvest credentials.
Recommended actions:
- Do **not** click the link
- Report the email as phishing
- Delete the message
- Access accounts only through the official Revolut site or app

---

## 👤 Author

Kishor — Cybersecurity Student
This repository is part of Task 2 submission.


