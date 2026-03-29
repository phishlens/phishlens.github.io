<p align="center">
  <img src="Phishlens.png" alt="PhishLens logo" width="160">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-MIT-green">
  <img src="https://img.shields.io/badge/version-v1.0.0-blue">
  <img src="https://img.shields.io/badge/type-client--side%20only-lightgrey">
</p>

PhishLens

PhishLens is a lightweight, browser-based phishing analysis tool for inspecting email headers and .eml files locally.

It helps analysts quickly review phishing indicators, investigate sender infrastructure, extract attachments, inspect archives, and safely download suspicious samples without relying on a backend.

------------------------------------------------------------

FEATURES

- Analyze raw email headers
- Upload and inspect .eml files locally
- Detect basic phishing indicators
- Brand impersonation hints
- Threat intelligence links for sender IPs
- Expand and review additional headers

ATTACHMENT FEATURES

- Extract attachments from uploaded .eml files
- Compute SHA-256 hashes for attachments
- Open attachment hashes in VirusTotal
- Detect suspicious file extensions
- Detect double extensions (e.g. invoice.pdf.exe)
- Inspect ZIP archives for risky contents
- Detect encrypted or password-protected ZIP files
- Download attachments as password-protected ZIP files

------------------------------------------------------------

IMPORTANT NOTE

Attachment extraction ONLY works when uploading a full .eml file.

- Pasting headers alone will NOT extract attachments
- Hash-only analysis does NOT extract attachments
- The MIME structure of the .eml file is required

------------------------------------------------------------

ATTACHMENT ANALYSIS

For each attachment, PhishLens shows:

- File name
- MIME type
- File size
- SHA-256 hash
- Risk level
- Risk reasons
- VirusTotal lookup link

------------------------------------------------------------

ATTACHMENT RISK CHECKS

PhishLens flags:

- Suspicious extensions:
  .exe, .js, .vbs, .bat, .cmd, .ps1, .hta, .iso, .img, .lnk

- Archive formats:
  .zip, .rar, .7z

- Double extensions:
  invoice.pdf.exe

- Suspicious MIME types
- Empty (0-byte) files

------------------------------------------------------------

ARCHIVE INSPECTION

For ZIP attachments:

- Lists files inside the archive
- Detects suspicious files inside ZIP
- Detects double extensions inside ZIP
- Flags encrypted entries
- Detects password-protected archives
- Performs limited nested ZIP inspection

------------------------------------------------------------

SAFE DOWNLOAD

Attachments are NOT downloaded raw.

They are automatically:

- Packaged into a ZIP file
- Protected with password:

  infected

This follows standard malware analysis practice and helps prevent accidental execution.

------------------------------------------------------------

PRIVACY

All analysis is performed locally in your browser.

- No headers are uploaded
- No attachments are uploaded
- No backend is used
- No APIs are required

Threat intelligence links are manual only.

------------------------------------------------------------

HOW TO USE

OPTION 1: HEADERS

1. Paste raw email headers
2. Click "Analyze"

OPTION 2: .EML FILE

1. Upload a .eml file
2. PhishLens will:
   - analyze headers
   - extract attachments
   - calculate hashes
   - inspect archives
   - provide safe downloads

------------------------------------------------------------

THREAT INTELLIGENCE LINKS

If an IP is found, links are provided for:

- AbuseIPDB
- VirusTotal
- GreyNoise
- Shodan
- Censys
- AlienVault OTX
- IPinfo
- Cisco Talos

------------------------------------------------------------

TECH STACK

- HTML
- CSS
- JavaScript
- zip.js (for password-protected ZIP downloads)

------------------------------------------------------------

DISCLAIMER

PhishLens is intended for:

- phishing analysis
- email forensics
- incident response
- defensive security research

Always handle suspicious files in a controlled environment.





