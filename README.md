# Vulnerability Management - Ticket / Project Summary Generator (VM-Assistant)

This web application helps generate ticket texts for vulnerability management using Ivanti and Rapid7. It supports CVE input, CSV upload, and auto-generates formatted outputs for ticketing and remediation.

## Features

- Enter CVE IDs manually or upload a CSV file containing vulnerability titles and/or CVE IDs.
- Fetches CVSS scores from NVD and determines risk/urgency.
- Generates Ivanti problem summary, Rapid7 query, and remediation project name.
- Provides a formatted description for ticketing, now showing vulnerability titles from the CSV (not just CVE IDs).
- If no titles are available, the app falls back to displaying CVE IDs in the description.
- Copy buttons for easy clipboard access.

## Usage

1. Open `VMAssistant.html` in Chrome.
2. Enter CVE IDs manually, or upload a CSV file with vulnerability titles (in a 'Title' column) and/or CVE IDs (in a 'Vulnerability Key' column or inside the title).
3. Fill in application name and other details.
4. Outputs are generated automatically.
5. Use copy buttons to transfer results.

## CSV Format

- The CSV should have a column named 'Title' containing vulnerability titles (with CVE IDs inside), or a 'Vulnerability Key' column containing CVE IDs.
- The app will extract CVE IDs for risk calculation and naming, and use the 'Title' column for the formatted description output.

## Requirements

- Chrome browser recommended.
- No server required; runs locally in browser.
- Internet connection required for CVSS score lookup.

## Notes

- Ad blockers may interfere; whitelist the domain if needed.
- Rate limits may be hit when too many queries are made to the NVD website.
