Task 4: Setup and Use a Firewall on Windows / Linux
Objective

Configure and test basic firewall rules to allow or block network traffic using:

      * Windows Defender Firewall (Windows)

      * UFW (Uncomplicated Firewall) (Linux)

Tools Used

     1] Windows Defender Firewall with Advanced Security

     2] UFW (Uncomplicated Firewall) on Linux (Ubuntu / Kali / Debian-based)

How a Firewall Filters Traffic (Summary)

A firewall works by inspecting network packets and applying rules based on:

Source IP

Destination IP

Port number

Protocol (TCP/UDP)

Direction (Inbound / Outbound)

Firewall Decision Flow
Packet arrives → Rule check → Allow or Block

Example

Port 23 (Telnet) → Blocked → ❌

Port 22 (SSH) → Allowed → ✅

Firewalls improve security by preventing unauthorized access, malware communication, and network attacks.
