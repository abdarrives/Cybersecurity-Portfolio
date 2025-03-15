# Windows Firewall Security Rules

## Overview
Blocking ICMP traffic is an essential security measure to prevent unauthorized network reconnaissance. In this project, I implemented Windows Firewall rules to block ICMP requests to external IPs.

### 🔐 Windows Firewall Security Rules – ICMP Blocking & Traffic Control
📌 Overview
ICMP (Internet Control Message Protocol) is a crucial network protocol used for diagnostics and troubleshooting. However, it can also be leveraged for network reconnaissance, ping sweeps, and denial-of-service (DoS) attacks.

To enhance network security and mitigate unauthorized ICMP traffic, I implemented Windows Firewall security rules to block ICMP requests to specific external IPs. This hands-on project involved:
✔️ Configuring custom firewall rules for inbound and outbound ICMP traffic.
✔️ Testing rule effectiveness by attempting various ping and network connectivity scenarios.
✔️ Capturing and analyzing network packets in Wireshark to verify the firewall behavior.

#### 🛠 Firewall Rule Configuration
🔹 ICMP Blocking Rule Details
🔥 Rule Name: Block ICMP to External Networks
🛡 Action: Block
📡 Protocol: ICMPv4
🎯 Scope: Selected external IPs (e.g., Google Public DNS – 8.8.8.8)
📌 Direction: Outbound (Prevent sending ICMP requests to blocked destinations)
🔹 Steps Taken:
* Navigated to Windows Firewall Advanced Security Panel
* Created a New Outbound Rule
* Chose Custom Rule → Selected ICMPv4 as protocol
* Scoped it to Google’s DNS (8.8.8.8)
* Set Action to Block
* Applied & Tested the Rule
* Attempted to ping 8.8.8.8 (should be blocked)
* Monitored packets using Wireshark
* Verified firewall logs for blocked attempts

##### 📸 Screenshots & Proof of Concept are attached


###### 📝 Lessons Learned & Key Takeaways
🔍 Understanding Firewall Traffic Control
Configuring outbound ICMP blocking can prevent information leaks via ping requests.
Inbound blocking prevents attackers from using ping sweeps to map active hosts on a network.

🛡 Firewall Rule Persistence
Rules must be saved and tested across system reboots to ensure they remain active.
Backup firewall configurations to quickly restore security settings when needed.

📊 Traffic Analysis with Wireshark
Live packet capture confirmed that outbound ICMP requests were blocked successfully.
No response packets were received, validating that the firewall rule was applied correctly.

⚠️ Understanding ICMP Blocking Side Effects
Completely blocking ICMP can cause unintended connectivity issues (e.g., breaking traceroute).
It's best to block selective ICMP types based on security needs rather than a full ICMP lockdown.
