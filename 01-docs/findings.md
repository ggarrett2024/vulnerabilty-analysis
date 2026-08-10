# Findings

This section documents the primary results identified during vulnerability scanning of the available virtual machines. The findings focus on host availability, exposed ports, network filtering, and differences observed between the scanned systems.

## `mandia_ftp_3`

The `mandia_ftp_3` system was reachable and responded to network scanning.

Port scanning identified multiple open TCP ports on the system. These open ports represented services available for network communication and therefore contributed to the system's exposed attack surface. Any unnecessary open ports could potentially be closed to reduce network exposure.

Additional scanning reported the examined ports as **unfiltered**, indicating that packet filtering was not preventing the scan probes from reaching them.

The system was also identified as **Microsoft Windows Longhorn**. Compared with `win-hunt-3`, `mandia_ftp_3` showed substantially more closed ports and less filtering.


## `win-hunt-3`

The scan of `win-hunt-3` produced a substantially different port profile.

The results identified:

* **13 open ports**
* **0 closed ports**
* **65,522 filtered ports**

The large number of filtered ports was the most noticeable difference compared with `mandia_ftp_3`. The results indicated that the majority of ports were being filtered rather than directly exposed or reported as closed.


## `win-xp-3`

The `win-xp-3` system could not be evaluated in the same way as the other targets because it was unavailable during the project.

The host was reported as down, and subsequent scanning did not provide additional information. Because no meaningful vulnerability or port information could be collected, the system was excluded from the final comparison.


## Comparison of Scan Results

The most significant difference between the successfully scanned systems was their port-filtering behavior.

`mandia_ftp_3` exposed multiple TCP ports and returned considerably more closed ports. Its ACK scan also showed the examined ports as unfiltered.

In contrast, `win-hunt-3` returned only 13 open ports while **65,522 ports were filtered**. This indicated a substantially different level of network filtering between the two systems.

Most of the open ports identified during the project were TCP ports. Because TCP ports provide network endpoints for applications and services, identifying unnecessary exposure is an important part of evaluating a system's security.


## Security Significance

The scan results demonstrated how port exposure and filtering can affect the visible attack surface of a system.

Open ports may support legitimate network services, but they can also create additional opportunities for unauthorized access when unnecessary or vulnerable services are exposed. Reviewing which ports are available and determining whether they are required can therefore support preventative security efforts.

The differences between `mandia_ftp_3` and `win-hunt-3` also showed how firewall behavior and system configuration can significantly change what is visible during a vulnerability scan.
