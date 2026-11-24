CyberDefenders – PhishStrike Lab

Platform: CyberDefenders
Category: Threat Intelligence
Path: SOC Analyst Tier 2 – Level 2
Difficulty: Medium
Estimated Time: 1 Hour
Status: Completed (11/11)

1. Lab Overview

The PhishStrike Lab focuses on investigating a phishing email targeting faculty members at an educational institution.

The email impersonated a trusted contact and claimed a fraudulent $625,000 purchase, providing a malicious invoice download link.

The objective was to analyze email headers, investigate malicious URLs, identify malware families, examine persistence mechanisms, and extract actionable Indicators of Compromise (IOCs).

2. Investigation & Findings

Q| Investigation| Finding

Q1| Sender IP (SPF softfail / DKIM fail)| "18.208.22.104"

Q2| Return-Path| "erikajohana.lopez@uptc.edu.co"

Q3| Malware Hosting IP| "107.175.247.199"

Q4| Cryptocurrency Malware Family| "CoinMiner"

Q5| Malware Requested URL| "http://ripley.studio/loader/uploads/Qanjttbv.jpeg"

Q6| BitRAT Persistence Executable| "jzwwix.exe"

Q7| Downloaded File SHA-256| "bf7628695c2df7a3020034a065397592a1f8850e59f9a448b555bc1c8c639539"

Q8| BitRAT Loader Download URL| "http://107.175.247.199/loader/server.exe"

Q9| PowerShell Execution Delay| "50 seconds"

Q10| BitRAT C2 Domain| "gh0st.mywire.org"

Q11| AsyncRAT Telegram Bot ID| "bot5609920260"


3. Evidence & Screenshots

Q1 – Email Header Analysis

Identified the sender's IP address using SPF and DKIM authentication results.

Evidence:

"Q1 Evidence" 

<img width="1920" height="490" alt="Screenshot (84)" src="https://github.com/user-attachments/assets/cdce7f18-96da-47c2-baa9-79f80152efa9" />




Q2 – Return-Path Analysis

Extracted the Return-Path email address to help trace the email source.

Evidence:

"Q2 Evidence" 

<img width="1920" height="512" alt="Screenshot (85)" src="https://github.com/user-attachments/assets/924629ae-6b37-4e1b-b2f4-c70cac5ed917" />


Q3 – Malware Hosting Infrastructure

Identified the IP address hosting the malicious malware distribution file.

Evidence:

"Q3 Evidence" 

<img width="1920" height="973" alt="Screenshot (86)" src="https://github.com/user-attachments/assets/14c9788f-4f9e-43e0-ad9a-a633ab92e5a8" />


Q4 – Cryptocurrency Mining Malware

Identified CoinMiner as the malware family responsible for cryptocurrency mining.

Evidence:

"Q4 Evidence" 

<img width="854" height="686" alt="Screenshot (95)" src="https://github.com/user-attachments/assets/24c7cc10-b534-4309-8046-4e23b7da5b7e" />



Q5 – Malicious URL Analysis

Identified the URL requested by the cryptocurrency malware.

Evidence:

"Q5 Evidence" 

<img width="1807" height="862" alt="Screenshot (87)" src="https://github.com/user-attachments/assets/eb698980-d96d-47a0-95b7-d49845a4728c" />


Q6 – Registry Persistence

Identified the executable added to the Windows Registry AutoRun key by BitRAT.

Evidence:

"Q6 Evidence" 

<img width="1809" height="743" alt="Screenshot (88)" src="https://github.com/user-attachments/assets/65d9b444-c6d8-432b-849a-190759304225" />


Q7 – File Hash Identification

Extracted the SHA-256 hash of the downloaded malicious executable.

Evidence

:"Q7 Evidence"

<img width="1799" height="719" alt="Screenshot (89)" src="https://github.com/user-attachments/assets/0dc75810-e68d-4f6b-8083-8742b50a56c7" />



Q8 – Malware Download Request

Identified the HTTP URL used by the loader to download BitRAT.

Evidence:

"Q8 Evidence" 

<img width="1867" height="375" alt="Screenshot (90)" src="https://github.com/user-attachments/assets/9ea0a5a1-71f8-4d2d-ac8b-66caf1079a01" />


Q9 – PowerShell Execution Analysis

Identified a 50-second delay in the PowerShell command execution.

Evidence:

"Q9 Evidence" 

<img width="1920" height="809" alt="Screenshot (91)" src="https://github.com/user-attachments/assets/d987ba54-57d1-498d-bd2e-8b1e2eda7627" />



<img width="1920" height="956" alt="Screenshot (92)" src="https://github.com/user-attachments/assets/4602d452-e7dc-4b6d-a80d-c847e5a7be44" />



Q10 – Command and Control (C2)

Identified the C2 domain used by BitRAT.

Evidence:

"Q10 Evidence" 

<img width="1078" height="934" alt="Screenshot (93)" src="https://github.com/user-attachments/assets/a7585daa-1165-4aa9-9a21-516a5f518d7e" />


Q11 – AsyncRAT Exfiltration

Extracted the Telegram Bot ID associated with AsyncRAT.

Evidence:

"Q11 Evidence" 

<img width="1481" height="631" alt="Screenshot (94)" src="https://github.com/user-attachments/assets/e283b237-8709-43bd-a554-b9139f6eace9" />



4. Tools & Techniques

Tools Used:

- Email Header Analyzer
- URLHaus
- URLScan.io
- VirusTotal
- MalwareBazaar
- VMRay

Technical Skills:

- Email Header Analysis
- SPF and DKIM Authentication Analysis
- Phishing Investigation
- Malicious URL Analysis
- Threat Intelligence and IOC Extraction
- Malware Family Identification
- Windows Registry Persistence Analysis
- SHA-256 Hash Analysis
- PowerShell Behavior Analysis
- Command and Control (C2) Identification

5. Conclusion

Successfully completed the investigation by analyzing phishing email headers, identifying malicious infrastructure, examining malware behavior, discovering persistence mechanisms, and extracting actionable IOCs.

This lab provided practical experience in phishing investigation, malware analysis, and threat intelligence, strengthening SOC Analyst skills in identifying and investigating email-based threats.

Final Result: 11/11 Questions Completed.
