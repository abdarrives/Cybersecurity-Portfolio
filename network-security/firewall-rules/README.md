# Windows Firewall Security Rules

## Overview
Blocking ICMP traffic is an essential security measure to prevent unauthorized network reconnaissance. In this project, I implemented Windows Firewall rules to block ICMP requests to external IPs.

## Firewall Rule Configuration
- **Rule Name:** Block ICMP to Google  
- **Action:** Block  
- **Protocol:** ICMPv4  
- **Scope:** Google IPs (8.8.8.8)  

### **Screenshots**
Screenshots are attached

## **Lessons Learned**
- Configuring outbound rules in Windows Firewall to block network traffic.
- Ensuring firewall settings persist across system reboots.
- Understanding the impact of ICMP blocking on network communication.

