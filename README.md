# Azure RDP Honeypot & Log Analytics Investigation Lab

## Overview

This project documents a controlled Azure honeypot lab designed to observe and analyze unauthorized Remote Desktop Protocol (RDP) login attempts against a publicly exposed Windows virtual machine.

The goal was to deploy a cloud-based VM, temporarily expose RDP to the internet, collect authentication logs in Azure Log Analytics, analyze failed login attempts using KQL, and document mitigation steps.

---

## Lab Architecture

```text
Internet
   |
   | TCP/3389 RDP
   v
Azure Network Security Group
   |
   v
Windows Virtual Machine
   |
   | Windows Event Logs
   v
Log Analytics Workspace
   |
   v
KQL Investigation

## Technologies Used
Microsoft Azure
Azure Virtual Network
Azure Virtual Machine
Network Security Group
Log Analytics Workspace
Azure Monitor Agent / Data Collection Rule
Kusto Query Language (KQL)
Windows Event Logs

## Objectives
Deploy a Windows VM in Azure
Temporarily expose RDP over TCP/3389
Collect Windows authentication logs
Identify failed RDP login attempts
Review successful logons for suspicious activity
Analyze source IPs and attack volume
Apply mitigation by restricting or removing public RDP access
Key Findings
