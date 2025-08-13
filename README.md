# Vulnerability Management - Ticket / Project Summary Generator (VM-Assistant)

This web application helps generate ticket texts for vulnerability management using Ivanti and Rapid7. It supports CVE input, CSV upload, and auto-generates formatted outputs for ticketing and remediation.

## Features

- Enter CVE IDs manually or upload a CSV file.
- Fetches CVSS scores from NVD and determines risk/urgency.
- Generates Ivanti problem summary, Rapid7 query, and remediation project name.
- Provides a formatted description for ticketing.
- Copy buttons for easy clipboard access.

## Usage

1. Open `VMAssistant.html` in Chrome.
2. Enter CVE IDs or upload a CSV.
3. Fill in application name and other details.
4. Outputs are generated automatically.
5. Use copy buttons to transfer results.

## Requirements

- Chrome browser recommended.
- No server required; runs locally in browser.

## Notes

- Ad blockers may interfere; whitelist the domain if needed.
- Rate limits may be hit when too many queries are made to the NVD website.
