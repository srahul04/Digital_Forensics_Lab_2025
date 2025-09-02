# Analyze Email Headers and Detect Email Spoofing Using MHA (Mail Header Analyzer)

## Aim
The aim of this experiment is to analyze email headers using Mail Header Analyzer (MHA) to detect email spoofing and determine the authenticity of emails by inspecting metadata and authentication results.

## Description
Email header analysis helps trace the path and legitimacy of an email from sender to receiver. Mail Header Analyzer (MHA) allows investigators to inspect key header fields, such as `From`, `Return-Path`, `Received`, `Message-ID`, and SPF/DKIM/DMARC results, to identify anomalies, irregular routing, and possible spoofing attempts. This experiment emphasizes the importance of verifying email origins to prevent phishing and unauthorized access.

## Procedure
1. Access the full raw email header from different email services:
   - Gmail: "Show original"
   - Outlook: "Properties" → "Internet headers"
   - Yahoo: "View raw message"
2. Copy the entire header text for offline analysis.
3. Examine important fields including `From`, `To`, `Date`, `Subject`, `Return-Path`, `Received`, `Message-ID`, and authentication results.
4. Analyze the `Received` fields to trace the path of the email from the last received server to the original sender.
5. Verify IP addresses and hostnames using WHOIS and IP lookup tools to check for geographical and ownership inconsistencies.
6. Inspect SPF, DKIM, and DMARC results to confirm whether the sending IP is authorized and the message integrity is maintained.
7. Analyze the `Message-ID` for domain mismatches that may indicate spoofing.
8. Identify anomalies such as mismatched domains, unusual IPs, or time discrepancies.
9. Optionally, use online tools like MXToolbox or Google’s G Suite Toolbox for automated header parsing.
10. Document all findings, noting suspicious elements and potential spoofing attempts, and report to IT or email providers if necessary.

## Result
The experiment showed that careful analysis of email headers using MHA can reveal signs of email spoofing. Suspicious patterns such as mismatched domains, unexpected IP addresses, or SPF/DKIM/DMARC failures were successfully identified, highlighting the effectiveness of header analysis in verifying email authenticity and preventing phishing attacks.
