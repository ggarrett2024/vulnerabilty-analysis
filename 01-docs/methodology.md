# Methodology

This section outlines the process used to perform vulnerability scanning across the available virtual machines using Nmap on Windows and SPARTA on Kali Linux.

## Environment

The project used Windows and Kali Linux virtual machines to perform network-based vulnerability analysis against several target systems.

The primary targets were:

* `mandia_ftp_3`
* `win-xp-3`
* `win-hunt-3`

The analysis focused on determining host availability, identifying accessible ports, and reviewing network information returned by the scanning tools.

## Nmap Scanning

Nmap was first used from the Windows virtual machine against `mandia_ftp_3`.

The initial scan was:

```bash
nmap -sn 172.16.3.242
```

This host-discovery scan was used to confirm that the target was reachable before continuing with additional scanning.

A TCP SYN scan was then performed:

```bash
nmap -sS 172.16.3.242
```

This scan was used to identify TCP ports available on the target.

A TCP ACK scan was also performed:

```bash
nmap -sA 172.16.3.242
```

This scan was used to examine how the target handled the probes and provide additional information related to port filtering.

## SPARTA Scanning

After completing the Nmap scans, the analysis moved to the Kali Linux virtual machine.

The IP address for `mandia_ftp_3` was added to SPARTA as the target host. The configured options automatically initiated:

* Nmap host discovery
* Staged Nmap scanning

After the scan completed, the available host, port, and service information was reviewed within the SPARTA interface.

## Windows XP Scan Attempt

The same general Nmap process was then attempted against `win-xp-3` using:

```bash
nmap -sn 172.16.3.213
```

The host-discovery scan was performed first to determine whether the system was available for further testing.

Additional scans were attempted after the host-discovery check, but the target remained unavailable. Because the system could not be reached, no further analysis could be completed against it.

## `win-hunt-3` Scanning

The analysis then returned to Kali Linux, where `win-hunt-3` was added to SPARTA as the target host.

SPARTA was allowed to complete its automated scanning process, after which the resulting host and port information was reviewed.

The results from the successfully scanned systems were then compared to identify differences in network exposure and filtering.

## Analysis Approach

A consistent scanning process was used where possible so the results from different systems could be compared more meaningfully.

The overall workflow was:

1. Identify the target system.
2. Confirm host availability where applicable.
3. Perform TCP-based port scanning.
4. Review open, closed, or filtered port information.
5. Examine available host and service details.
6. Compare the successfully scanned systems.

The unavailable Windows XP system was excluded from the final comparison because it did not return enough information for meaningful analysis.
