# OpenVAS-Local-Host-Scan
A report detailing the findings of a vulnerability assessment performed on a local host using the OpenVAS scanner.
1. Overview
The primary objective of this task was to use a free vulnerability scanning tool to identify common security risks on my local computer. For this assessment, I used 
OpenVAS (Greenbone Vulnerability Manager) deployed on a Kali Linux system. The scan was performed against my local PC, identified by the IP address 192.168.1.20.
The scan completed successfully, and the final report indicated that there were no vulnerabilities of Low, Medium, or High severity found from a network perspective.

2. Scan Process
The process of completing this task involved several key stages:
Installation & Setup: The Greenbone Vulnerability Manager (GVM) framework was installed on a Kali Linux environment. The setup involved a lengthy synchronization process to download the latest vulnerability information feeds (NVTs, SCAP, etc.). Several troubleshooting steps were required to resolve issues related to disk space, service permissions, and feed synchronization.
Target Definition: A target was created within OpenVAS, pointing to the local IP address 192.168.1.20, as specified in the task guide.
Scan Execution: A "Full and fast" uncredentialed scan was configured and launched against the defined target. The scan was monitored until completion.
Analysis & Reporting: The final report was analyzed to review the findings. All identified items were informational logs rather than actionable vulnerabilities.

3. Scan Results & Findings
The scan concluded that the target host, 192.168.1.20, was not vulnerable to any of the checks performed by the scanner. All results were informational logs with a severity of 0.0 (Log).

This indicates that from an external network perspective, the machine has a secure perimeter.



The informational findings included:
Finding	Severity	Description
OS Detection	0.0 (Log)	The scanner attempted to identify the operating system of the target machine.
Hostname Determination	0.0 (Log)	The scanner identified the hostname associated with the target IP.
Traceroute	0.0 (Log)	The scanner determined the network path to the target machine.
CPE Inventory	0.0 (Log)	The scanner created an inventory of services using the Common Platform Enumeration format.
4. Analysis: Uncredentialed Scan
The primary reason for the "clean" report is the type of scan that was performed. This was an uncredentialed scan, meaning the scanner had no login credentials for the target machine. It assessed the PC from an outsider's perspective.

This type of scan can identify network-level vulnerabilities but cannot see local issues like:

Missing security patches for the operating system.

Outdated versions of installed software (e.g., browsers, office suites).



This is a great choice because it's clear, includes the task number, and is easy for your reviewers to identify.
