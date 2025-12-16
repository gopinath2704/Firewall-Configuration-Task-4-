Windows Firewall Configuration
1. Open Windows Firewall

Press Win + R

Type wf.msc

Press Enter

➡️ Opens Windows Defender Firewall with Advanced Security

📸 Screenshot 1: Windows Firewall main window

![alt text](New-inbound-rule-Windows-Defender-Firewall.png)

2. List Current Firewall Rules

Click Inbound Rules

Observe existing rules (HTTP, HTTPS, SMB, etc.)

📸 Screenshot 2: Existing Inbound Rules list

![alt text](windows-defender-firewall-inbound-rules.jpg)

3. Add Rule to Block Inbound Traffic (Port 23 – Telnet)

Click Inbound Rules

Click New Rule

Select Port → Next

Choose TCP

Specific local ports: 23

Select Block the connection

Apply to Domain, Private, Public

Name the rule:
Block Telnet Port 23

Click Finish


4. Test the Firewall Rule
Using Command Prompt
telnet localhost 23

✅ Connection should fail

📸 Screenshot 3: Failed Telnet connection

![alt text](<Screenshot 2025-12-16 070136.png>)

5. Remove the Test Rule

Go to Inbound Rules

Right-click Block Telnet Port 23

Click Delete
