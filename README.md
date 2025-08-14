# Vulnerability Management - Ticket / Project Summary Generator (VM-Assistant)

This web application helps generate ticket texts for vulnerability management using Ivanti and Rapid7. It supports CVE input, CSV upload, and auto-generates formatted outputs for ticketing and remediation.

## Features

- Enter CVE IDs manually or upload a CSV file containing vulnerability titles and/or CVE IDs.
- When uploading a CSV, CVSS scores are extracted directly from the 'CVSS Score' column (no external lookup required).
- If CVE IDs are entered manually, CVSS scores are fetched from the NVD website.
- Generates Ivanti problem summary, Rapid7 query, and remediation project name.
- Provides a formatted description for ticketing, showing vulnerability titles from the CSV (not just CVE IDs).
- If no titles are available, the app falls back to displaying CVE IDs in the description.
- Copy buttons for easy clipboard access.

## Usage

1. Open `VMAssistant.html` in Chrome.
2. Enter CVE IDs manually, or upload a CSV file with vulnerability titles (in a 'Title' column), CVE IDs (in a 'Vulnerability Key' column or inside the title), and optionally CVSS scores (in a 'CVSS Score' column).
3. Fill in application name and other details.
4. Outputs are generated automatically.
5. Use copy buttons to transfer results.

## CSV Format

- The CSV should have a column named 'Title' containing vulnerability titles (with CVE IDs inside), a 'Vulnerability Key' column containing CVE IDs, and a 'CVSS Score' column containing the CVSS base score for each vulnerability.
- The app will extract CVE IDs for risk calculation and naming, use the 'Title' column for the formatted description output, and use the 'CVSS Score' column for risk/urgency calculation when available.

## Requirements

- Chrome browser recommended.
- No server required; runs locally in browser.
- Internet connection required for CVSS score lookup (manual CVE entry only).

## Notes

- Ad blockers may interfere; whitelist the domain if needed.
- Rate limits may be hit when too many queries are made to the NVD website (manual CVE entry only).
