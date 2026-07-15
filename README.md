An outstanding and highly practical guide to Google Dorking has been synthesized into a structured, production-ready GitHub README.md file content below. This layout is optimized for developers and security researchers, featuring clean markdown structure, a clear directory-like table of contents, and highlighted key warnings.-----
# Crash Dork Secrets: Ethical Public Information Gathering

> [!WARNING]  
> **Ethical Use Only:** This guide is designed to help you check if your own personal information is exposed on the internet, identify digital footprint leaks, and secure your personal privacy. Use these techniques responsibly and ethically.

---

## ðŸ“– About the Guide
This repository contains a curated cheat sheet of Google Dork queries designed to help individuals audit their online exposure and monitor their digital footprint. By utilizing advanced search operators, you can identify accidental data leaks of names, emails, phone numbers, and sensitive documents across the web.

---

## ðŸ› ï¸ Core Google Dorks Operators Reference

Google Dorks leverage advanced search operators to filter index databases with high precision.

| Operator | Purpose | Example | Explanation |
| :--- | :--- | :--- | :--- |
| `site:` | Restrict results to a specific domain or TLD. | `site:[link removed]` | Searches only within *[link removed]*. |
| `filetype:` | Search for specific file extensions. | `filetype:pdf` | Displays indexed PDF files. |
| `inurl:` | Filter pages containing target terms in the URL. | `inurl:admin` | Finds URLs containing "admin". |
| `intitle:` | Look for specific keywords inside page titles. | `intitle:"login"` | Returns pages with "login" in the title. |
| `intext:` | Locate exact phrases inside the page body text. | `intext:"username password"` | Targets pages containing the phrase "username password". |

---

## ðŸ” Cheat Sheet Queries

### 1. File and Document Auditing
Locate accidentally exposed documents containing personal names or private details.
*   `"<Name>" filetype:pdf OR filetype:doc OR filetype:xlsx`
*   `site:[link removed] filetype:pdf` (Audit specific domains for files)
*   `intitle:"login"` (Exposed credentials or text logs)

### 2. Personal Information Leak Testing
Check if your identity elements are combined and publicly crawlable.
*   `intext:"<Name>" intext:"<Email>" intext:"<Phone>"`

### 3. Professional & Social Profiling
Locate precise online identities and profiles across platform indexes.
*   **LinkedIn:** `"<Name>" site:[link removed]`
*   **Facebook:** `"<Name>" site:[link removed]`
*   **Twitter:** `"<Name>" site:[link removed]`
*   **Instagram:** `"<Name>" site:[link removed]`

### 4. Direct Email & Contact Harvesting Protection
Audit contact lists or raw database drops indexing your contact addresses.
*   `"<Name>" email OR contact`
*   `"<Name>" "@gmail.com" OR "@yahoo.com"`
*   `"<Name>" site:[link removed]` (Detect pastebin and raw log exposures)

### 5. Academic & Research Discovery
Find institutional files, research projects, or university listings.
*   **ResearchGate:** `"<Name>" site:researchgate.net`
*   **Google Scholar:** `"<Name>" site:[link removed]`
*   **Universities:** `"<Name>" site:edu`

### 6. Corporate & Organization Repositories
Identify startup registrations, employee registries, and platform codes.
*   **Crunchbase:** `"<Name>" site:[link removed]`
*   **AngelList:** `"<Name>" site:angel.co`
*   **GitHub:** `"<Name>" site:[link removed]`

### 7. Breach & Leak Tracking
Trace records of credentials appearing in leaked database dumps.
*   `"<Name>" site:[link removed]`
*   `"<Name>" inurl:leak OR inurl:dump`

### 8. Legal & Government Mentions
Identify court docket appearances or regulatory notifications.
*   **Government Sites:** `"<Name>" site:gov.in OR site:gov`
*   **Legal Cases (India):** `"<Name>" court case OR litigation site:indiankanoon.org`

### 9. Advanced OSINT Queries
Advanced queries for targeting broad file shares or resume metadata.
*   **Resumes:** `"<Name>" intitle:"resume"`
*   **Slide Decks:** `"<Name>" site:slideshare.net`
*   **Exposed Drive Files:** `"<Name>" site:[link removed]`
*   **Profiles:** `"<Name>" intitle:"profile" OR inurl:"profile"`
*   **Location Constraints:** `"<Name>" AND "<City/State>"`
*   **Phone Matches:** `"<Name>" AND "phone" OR "mobile"`

