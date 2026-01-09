# SOC-Incident-Triage-Threat-Analysis
This repository documents hands-on Security Operations Center (SOC) investigations involving phishing emails, malicious URLs, and firewall detections. All cases were analyzed using SIEM telemetry to determine True Positives vs False Positives, validate hypotheses, and assess impact.
Investigation Workflow

Alert Review – Email, firewall, or proxy alert ingestion

IOC Identification – URLs, domains, IPs, sender artifacts

Log Correlation – Email + firewall telemetry

Classification – True Positive (TP) or False Positive (FP)

Impact Assessment – Prevented vs potential compromise

SOC Reporting – Clear, concise incident conclusions

 Case Summaries
Case 1: Amazon Delivery Phishing

Type: Phishing (TP)

Indicators:

Sender spoofing (amazon.biz)

Shortened malicious URL (bit.ly)

Urgency-based social engineering

Outcome: Confirmed phishing attempt

Impact: None (user did not interact)

Case 2: Microsoft Account Impersonation

Type: Phishing (TP)

Indicators:

Typosquatted domain (m1crosoftsupport.co)

Fake security alert

Credential-harvesting login link

Outcome: Confirmed phishing attempt

Impact: None observed

Case 3: Blocked Malicious URL

Type: Prevented Threat (TP)

Indicators:

Known malicious shortened URL

Firewall block enforced

Outcome: Outbound connection blocked

Impact: None (prevented at perimeter)

Case 4: HR Onboarding Email

Type: False Positive (FP)

Indicators:

Sender and link domain match

Legitimate internal workflow

Outcome: Benign business email

Impact: None

Tools & Techniques

SIEM Analysis (Splunk-style workflow)

Email Security Triage

Firewall & Proxy Log Review

IOC Enumeration

Threat Classification (TP vs FP)

SOC Incident Reporting

Key Takeaways

Logs and behavior outweigh threat intel alone

Domain analysis and link inspection are critical for phishing detection

Prevented events still count as True Positives

Accurate triage reduces alert fatigue and false escalations

Analyst Conclusion

All alerts were successfully investigated and classified using SOC-standard methodology. Confirmed threats were either prevented by security controls or identified before user interaction, demonstrating effective detection and response.
