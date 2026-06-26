# Enterprise SOC Lab

A practical cybersecurity training lab focused on basic SOC operations, network monitoring, endpoint visibility, and incident response documentation.

This project is part of my hands-on learning journey in cybersecurity after completing a cybersecurity training diploma. The goal is to understand how security tools work together in a small lab environment and to document the process clearly.

This is not a production SOC environment. It is a learning lab designed to demonstrate practical understanding, troubleshooting ability, and basic security operations skills.

## Project Goal

The goal of this lab is to practice the core skills needed for entry-level SOC, IT security, and infrastructure support roles.

Main learning goals:

* Understand basic network design
* Configure a firewall gateway
* Monitor Windows and Linux systems
* Collect and review security logs
* Analyze IDS alerts
* Practice alert triage
* Write basic investigation notes
* Build clear technical documentation

## Lab Architecture

```text
Internet / NAT
    |
OPNsense Firewall
    |
Internal LAN: 192.168.50.0/24
    |
    |-- SOC-01 Ubuntu Server / Wazuh Manager: 192.168.50.10
    |-- USER01 Windows Endpoint: 192.168.50.20
    |-- TEST01 Testing Machine: 192.168.50.30
```

## Tools Used

* OPNsense Firewall
* Wazuh SIEM
* Suricata IDS
* Wireshark
* Windows Endpoint
* Ubuntu Server
* VMware
* Linux CLI
* PowerShell
* GitHub Documentation

## What I Implemented

* Built an internal lab network using VMware
* Configured OPNsense as the main firewall and gateway
* Created basic firewall rules for internal network traffic
* Installed Wazuh Manager on Ubuntu Server
* Installed Wazuh Agent on a Windows endpoint
* Verified endpoint visibility inside Wazuh
* Enabled Suricata IDS on the LAN interface
* Downloaded and enabled selected ET Open rules
* Generated and reviewed Suricata network alerts
* Started documenting alert triage and investigation steps

## Current Lab Status

Completed:

* Internal network design
* OPNsense firewall setup
* Windows endpoint setup
* Ubuntu SOC server setup
* Wazuh installation
* Windows Wazuh Agent connection
* Suricata IDS setup
* Initial network alerts visible in OPNsense

In progress:

* Forwarding Suricata events into Wazuh
* Wireshark packet analysis notes
* Failed login investigation report
* Basic incident response documentation
* MITRE ATT&CK mapping practice
* Simple IOC documentation

## Example Network Alert

One of the first alerts observed in Suricata was related to DNS over HTTPS traffic:

```text
ET INFO Observed Cloudflare DNS over HTTPS Domain
ET INFO Observed Google DNS over HTTPS Domain
```

Initial analysis:

* Source: Windows endpoint
* Destination: Google / Cloudflare services
* Destination port: 443
* Action: Allowed
* Type: Informational
* Assessment: No immediate evidence of compromise. The alert was useful for understanding encrypted DNS behavior and network visibility.

## SOC Triage Process

For each alert, I try to review:

1. Hostname
2. Source IP
3. Destination IP
4. Port
5. Timestamp
6. Alert signature
7. Related logs
8. Initial assessment
9. Decision
10. Next action

## Planned Improvements

The next stages of this project will include:

* Sending Suricata events into Wazuh
* Creating a Wireshark packet analysis lab
* Documenting a failed login investigation
* Writing a Suricata alert analysis report
* Building simple SOC playbooks
* Creating a basic MITRE ATT&CK mapping table
* Creating a small IOC table
* Preparing a final project summary suitable for a CV or interview discussion

## Learning Outcomes

Through this lab, I am improving my understanding of:

* How traffic moves through a firewall
* How endpoint logs reach a SIEM
* How IDS alerts help with network visibility
* How to separate informational alerts from suspicious activity
* How to document technical work clearly
* How to troubleshoot issues step by step
* How to explain a security lab in a professional and realistic way

## Notes

This project is a learning lab. It is not a production environment.

The purpose is to show practical understanding, discipline, troubleshooting ability, and documentation skills suitable for entry-level cybersecurity, SOC Analyst L1, IT security support, or infrastructure support roles.

