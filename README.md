# phishlens.github.io
# PhishLens

PhishLens is a lightweight, browser-based email header analysis tool built to help security analysts, blue teams, and researchers quickly triage potential phishing emails.

The tool runs entirely in the browser. No email data is sent to a server, no APIs are required, and no tracking is performed.

Live site:  
https://phishlens.github.io

---

## Overview

PhishLens focuses on fast and practical phishing analysis using email headers and `.eml` files.  
It highlights common indicators such as brand impersonation, suspicious subject language, and sender infrastructure, and provides direct links to well-known public threat intelligence platforms for manual investigation.

PhishLens is designed as a **decision-support tool**, not an automated detection engine.

---

## Features

- Paste raw email headers for analysis  
- Upload `.eml` files directly in the browser  
- Heuristic phishing risk scoring with explanations  
- Detection of common brand impersonation patterns  
- Extraction of sender IP from Received headers  
- Direct pivots to public threat intelligence platforms:
  - AbuseIPDB  
  - VirusTotal  
  - GreyNoise  
  - Shodan  
  - Censys  
  - AlienVault OTX  
  - IPinfo  
  - Cisco Talos  
- Optional dark mode  
- Fully client-side implementation (no backend)

---

## How It Works

All parsing and analysis is performed locally using JavaScript:

- Email headers are parsed in the browser  
- The Received chain is inspected to extract sender IPs  
- Simple heuristics are applied to identify common phishing indicators  
- No external services are contacted automatically  

This makes PhishLens safe to use with sensitive or internal email data.

---

## Usage

1. Open the live site at https://phishlens.github.io  
2. Paste raw email headers or upload a `.eml` file  
3. Click the Analyze button  
4. Review the risk score, indicators, and investigation links  

PhishLens is optimized for rapid triage rather than deep forensic reconstruction.

---

## Limitations

- The analysis is heuristic-based and not exhaustive  
- Not all phishing emails will be detected  
- Results should not be used as the sole basis for security decisions  

PhishLens works best when combined with additional context such as SIEM alerts, user reports, sandboxing, and endpoint telemetry.
