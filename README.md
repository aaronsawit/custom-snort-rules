
# Custom Snort Rules

This repository contains a set of custom Snort rules designed to detect various network activities and potential threats, such as ICMP requests, HTTP traffic with specific content, SQL injections, and more. These rules are tailored to monitor and alert on key activities within a network.

## Table of Contents

- [Installation](#installation)
- [Configuration](#configuration)
- [Rules Overview](#rules-overview)
- [Usage](#usage)

---

## Installation

1. Install Snort:
- Make sure Snort is installed on your system. You can find installation instructions on the official [Snort website](https://www.snort.org).

2. Clone this repository:
- git clone https://github.com/aaronsawit/custom-snort-rules
cd custom-snort-rules


---

## Configuration

1. Copy the `snort_rules.conf` file to your Snort rules directory.

2. Modify the Snort configuration (`snort.conf`):
- Include the custom rules in your `snort.conf` file. Add the following line to ensure Snort uses your custom rules:
 ```
 include /path/to/snort_rules.conf
 ```

3.  Logging:
- Ensure that Snort is configured to log alerts. You can set the output format by modifying your `snort.conf` file:
 ```
 output alert_fast: /var/log/snort/alerts.log
 ```

---

## Rules Overview

Here are the custom rules included in this repository:

### 1. Detect ICMP (ping) requests

### 2. Detect HTTP traffic containing a specific string in the payload

### 3. Detect SSH login attempts

### 4. Detect DNS queries for a malicious domain

### 5. Detect traffic from a specific IP

### 6. Detect FTP login attempts

### 7. Detect SQL Injection attempts

### 8. Detect Nmap scan attempts

### 9. Detect RDP brute force attempts

### 10. Detect HTTP POST requests

### 11. Detect executable file downloads over HTTP (.exe files)

### 12. Detect ARP spoofing


### 13. Detect more than 5 POST requests in 10 seconds

---

## Usage

To use the custom rules, follow these steps:

1. Run Snort with the custom rules:
- Make sure Snort is properly configured and the custom rules are included in the `snort.conf` file. Run Snort as follows:
 ```
 sudo snort -c /path/to/snort.conf -l /path/to/logs
 ```

2. Monitoring Alerts:
- The alert logs can be found in the directory you specified in the `snort.conf` file (e.g., `/var/log/snort/alerts.log`).

---

## Additional Notes

- You can modify or expand the rules based on your network needs.
- Ensure you have sufficient logging to track any events triggered by these rules.
