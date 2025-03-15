# Windows Firewall Security Rules

## Overview
Blocking ICMP traffic is an essential security measure to prevent unauthorized network reconnaissance. In this project, I implemented Windows Firewall rules to block ICMP requests to external IPs.

## Firewall Rule Configuration
- **Rule Name:** Block ICMP to Google  
- **Action:** Block  
- **Protocol:** ICMPv4  
- **Scope:** Google IPs (8.8.8.8)  

### **Screenshots**
1. **Firewall Rule Setup**
   - ![Firewall Rule](firewall_block_google.png)
2. **Ping Test (Blocked)**
   - ![Ping Failure](ping_test_blocked.png)
3. **Firewall Rule Backup**
   - ![Firewall Backup](firewall_backup.png)

## **Lessons Learned**
- Configuring outbound rules in Windows Firewall to block network traffic.
- Ensuring firewall settings persist across system reboots.
- Understanding the impact of ICMP blocking on network communication.

