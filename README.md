# Vulnerability Analysis

This portion of the portfolio demonstrates vulnerability analysis and network enumeration using Nmap and SPARTA across Windows and Kali Linux virtual machines.

The project focuses on identifying active hosts, examining exposed and filtered ports, reviewing network services, and comparing vulnerability-analysis tools across different systems.

## Why the Project Was Completed

Vulnerability analysis helps identify potential security weaknesses before they can be exploited. Information such as host availability, open ports, running services, and firewall filtering can provide insight into a system's security posture and potential attack surface.

The project was completed to gain practical experience using vulnerability-analysis tools and to examine how different systems respond to network scans.

## Tools and Technologies

### Nmap

Nmap was used from a Windows virtual machine for host discovery and port scanning. The project included ping scans, TCP SYN scans, and TCP ACK scans.

### SPARTA

SPARTA was used from Kali Linux to perform network discovery and staged Nmap scans through a graphical interface. It provided organized information about hosts, ports, services, and filtering.

### Additional Technologies and Concepts

* Kali Linux
* Windows
* TCP/IP
* Host discovery
* TCP SYN scanning
* TCP ACK scanning
* Port enumeration
* Network services
* Firewall filtering
* Virtual machines

## What the Work Involved

The project involved scanning multiple virtual machines with Nmap and SPARTA to determine whether hosts were active and examine their network exposure.

Nmap was used to perform host discovery and TCP-based port scans from Windows. SPARTA was then used from Kali Linux to perform automated discovery and staged scans while presenting the results through a graphical interface.

The scan results were compared to examine differences in open, closed, and filtered ports across the available systems. One Windows XP target was also tested but could not be analyzed further because the host was unavailable during the lab.

## Key Takeaways

The project demonstrated how vulnerability-analysis tools can provide visibility into active systems, exposed ports, available services, and network filtering.

It also provided experience comparing command-line and graphical scanning tools. Nmap offered direct control over individual scan types, while SPARTA simplified the scanning process by combining automated Nmap functionality with an organized graphical interface.

More detailed scan findings, system comparisons, and tool analysis are included in the supporting project documentation.


## Repository Sections

### `docs/`

The `docs` directory contains the summarized written documentation for the project. Each file focuses on a different part of the vulnerability-analysis process.

* `findings.md` documents the primary scan results, including host availability, exposed ports, filtering behavior, and differences identified between the successfully scanned systems.
* `methodology.md` explains the vulnerability-scanning process, including host discovery, TCP SYN scanning, TCP ACK scanning, SPARTA-based scanning, and the handling of an unavailable target system.
* `tool-comparison.md` compares Nmap and SPARTA based on interface, platform availability, automation, usability, scanning capabilities, and limitations.

### `images/`

The `images` directory contains selected screenshots extracted from the original report.

These images provide visual evidence of the Nmap and SPARTA scans discussed throughout the project documentation, including TCP port scanning, filtering analysis, and scan results from the evaluated systems. Only the most relevant figures were retained to keep the repository focused on the technical findings.

### `full-report/`

The `full-report` directory contains the sanitized version of the original lab report.

* `sanitized-lab-report.pdf` provides the original project narrative, technical background, scanning process, findings, tool comparison, figures, and references while removing personal or identifying information that should not appear in a public repository.

[Return to the Cybersecurity Portfolio](https://github.com/ggarrett2024/Cybersecurity-Portfolio)

