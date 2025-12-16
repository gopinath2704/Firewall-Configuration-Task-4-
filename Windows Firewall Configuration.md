Windows Firewall Configuration
1. Open Windows Firewall

Press Win + R

Type wf.msc

Press Enter

➡️ Opens Windows Defender Firewall with Advanced Security

📸 Screenshot 1: Windows Firewall main window

<img width="700" height="500" alt="New-inbound-rule-Windows-Defender-Firewall" src="https://github.com/user-attachments/assets/307da89f-bdde-4750-883e-b2838fec8052" />


2. List Current Firewall Rules

Click Inbound Rules

Observe existing rules (HTTP, HTTPS, SMB, etc.)

📸 Screenshot 2: Existing Inbound Rules list

![windows-defender-firewall-inbound-rules](https://github.com/user-attachments/assets/0f1685da-ef83-4c40-8760-774cac56bc1a)


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

<img width="1483" height="762" alt="Screenshot 2025-12-16 070136" src="https://github.com/user-attachments/assets/145d7326-a781-4142-82b2-5c710188dbf3" />


5. Remove the Test Rule

Go to Inbound Rules

Right-click Block Telnet Port 23

Click Delete

