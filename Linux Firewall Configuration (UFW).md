Linux Firewall Configuration (UFW)

1. Open Terminal
Ctrl + Alt + T

2. Check UFW Status
sudo ufw status verbose


If inactive:

sudo ufw enable


📸 Screenshot 6: UFW enabled

3. List Current Rules
sudo ufw status numbered


📸 Screenshot 7: Current UFW rules

4. Block Inbound Traffic on Port 23 (Telnet)
sudo ufw deny 23


OR explicitly:

sudo ufw deny 23/tcp


📸 Screenshot 8: Port 23 blocked

5. Allow SSH (Port 22)
sudo ufw allow 22


📸 Screenshot 9: SSH allowed

6. Test the Firewall Rule
Local Test
telnet localhost 23


OR

nc -zv localhost 23


Expected Output:

Connection refused


📸 Screenshot 10: Connection blocked

7. Remove the Test Block Rule
sudo ufw status numbered
sudo ufw delete <rule-number>


OR

sudo ufw delete deny 23


📸 Screenshot 11: Rule removed

Documentation of Commands Used (Linux)
sudo ufw enable
sudo ufw status
sudo ufw deny 23
sudo ufw allow 22
sudo ufw delete deny 23