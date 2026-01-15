# Web Reconnaissance Report

## Overview
This report documents a basic web reconnaissance assessment conducted against a legal test target. The objective was to identify exposed services, accessible directories, and common web server misconfigurations.

## Target
- testphp.vulnweb.com
- Scope limited to passive and non-intrusive scanning

## Tools Used
- Nmap
- Dirb
- Nikto

## Nmap Results
The scan identified multiple open ports exposing web services. Port 80 was found running nginx 1.19.0 over HTTP, which may expose unencrypted traffic and reveal server version information. Additional HTTP services were discovered on non-standard ports 8008 and 8010, increasing the overall attack surface.

## Directory Enumeration
Directory enumeration using a common wordlist did not reveal any accessible sensitive directories. The scan encountered connection timeouts, suggesting the presence of basic protections such as request filtering or rate limiting.

## Nikto Findings
A Nikto web server scan did not identify any critical vulnerabilities or high-risk misconfigurations. No known vulnerable files, insecure HTTP methods, or severe security header issues were detected, indicating basic web server hardening.

## Conclusion
While no critical vulnerabilities were identified, the target exposes multiple web services that increase its attack surface. It is recommended to minimize exposed services, enforce HTTPS, limit information disclosure, and continue monitoring for misconfigurations.
