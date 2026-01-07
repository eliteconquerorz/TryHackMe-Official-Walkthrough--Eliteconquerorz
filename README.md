# TryHackMe-Official-Walkthrough--Eliteconquerorz

Overview

This walkthrough covers the Phishing Email Analysis task on the TryHackMe platform. The objective is to examine a suspicious email, identify phishing indicators, analyze headers and attachments/links, and answer the related questions accurately. This exercise helps build real-world SOC and blue-team skills.
Learning Objectives

By the end of this walkthrough, you will be able to:

    Identify common phishing characteristics
    Analyze email headers to trace sender information
    Inspect URLs and attachments safely
    Extract Indicators of Compromise (IOCs)
    Classify the email as malicious or benign

Tools & Resources Used

    TryHackMe AttackBox (recommended)
    Email client or provided .eml file viewer
    Online header analyzers (manual analysis preferred)
    URL inspection techniques (without clicking)
    Hashing tools (if attachments are present)

Step 1: Initial Email Inspection

Start by reading the email carefully without clicking any links.
What to Look For

    Sender address: Does it look legitimate or spoofed?
    Display name vs email address mismatch
    Urgency or threats (“Act now”, “Account will be closed”)
    Spelling/grammar mistakes
    Unexpected attachments or links

    🚩 Phishing emails often create panic or curiosity to force quick action.

Step 2: Analyze the Email Headers

Email headers reveal how the email traveled from sender to recipient.
Key Header Fields

    From: Claimed sender
    Return-Path: Actual return address
    Received: Mail servers the email passed through
    SPF, DKIM, DMARC: Authentication results

Analysis

    Compare From and Return-Path
    Check if SPF/DKIM/DMARC failed
    Identify suspicious IP addresses or unknown mail servers

    ⚠️ Failed authentication checks strongly suggest spoofing.

Step 3: Link Analysis (Without Clicking)

Hover over links or inspect the raw email content.
Red Flags

    URL shortening services
        IP-based URLs instead of domain names
    Misspelled domains (e.g., paypa1.com)
    Mismatch between displayed text and actual URL

Common Malicious Attachments

    .html, .iso, .zip, .exe
    Office files requesting Enable Macros

Safe Analysis Steps

    Do not open directly
    Identify the file type
    Calculate hash (MD5/SHA256 if required)
    Look for misleading file names (e.g., Invoice.pdf.exe)

    📌 On TryHackMe, attachments are usually safe to analyze within the platform environment.

Step 5: Identify Indicators of Compromise (IOCs)

Collect all suspicious elements:

    Sender email address
    Malicious domain or URL
    IP address from headers
    Attachment hash

These IOCs are often required to answer the room questions.
Step 6: Answering TryHackMe Questions

Use your findings to answer:

    What is the sender’s email address?
    Is the domain spoofed or malicious?
    What authentication checks failed?
    What is the malicious URL or attachment hash?
    Is this email phishing or legitimate?

Double-check spelling and format, as answers are case-sensitive.
Final Verdict

Based on:

    Spoofed sender details
    Failed email authentication
    Suspicious links/attachments
    Social engineering tactics

👉 The email is classified as PHISHING.
Key Takeaways

    Never trust emails based on appearance alone
    Header analysis is critical for verification
    Phishing relies more on psychology than technology
    Always analyze links and attachments safely

Conclusion

This TryHackMe room provides hands-on experience in phishing detection, a critical skill for SOC analysts and cybersecurity professionals. Mastering these techniques helps prevent credential theft, malware infections, and data breaches in real environments.
