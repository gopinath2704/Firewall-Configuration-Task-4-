Linux Firewall Configuration (UFW)

1. Open Terminal
   
       Ctrl + Alt + T

2. Check UFW Status
   
        sudo ufw status verbose

  If inactive:

        sudo ufw enable


📸 Screenshot : UFW enabled

<img width="955" height="985" alt="UFW enabled" src="https://github.com/user-attachments/assets/bc783ea5-3978-466b-bb4a-aed3578493aa" />

 
3. List Current Rules
   
       sudo ufw status numbered


📸 Screenshot : Current UFW rules

<img width="1920" height="997" alt="Current UFW rules" src="https://github.com/user-attachments/assets/4c9ce39e-dede-453a-a618-163f0f581dd8" />


4. Block Inbound Traffic on Port 23 (Telnet)
   
        sudo ufw deny 23


  OR explicitly:

        sudo ufw deny 23/tcp


📸 Screenshot : Port 23 blocked

<img width="955" height="985" alt="Port 23 blocked" src="https://github.com/user-attachments/assets/2f48bba9-e837-469d-be9e-29d8f210ce4d" />


5. Allow SSH (Port 22)
   
        sudo ufw allow 22


📸 Screenshot : SSH allowed

<img width="955" height="985" alt="SSH allowed" src="https://github.com/user-attachments/assets/f04988a2-0d8a-41de-9aaf-0ad4052f4d0c" />


6. Test the Firewall Rule
   
Local Test

      telnet localhost 23


OR

      nc -zv localhost 23


Expected Output:

Connection refused


📸 Screenshot : Connection blocked

<img width="955" height="985" alt="Connection blocked" src="https://github.com/user-attachments/assets/cda94e0a-ffbb-420c-b7bc-347ab1eb3cad" />


7. Remove the Test Block Rule
   
       sudo ufw status numbered
       sudo ufw delete <rule-number>


   OR

       sudo ufw delete deny 23


📸 Screenshot : Rule removed

<img width="955" height="985" alt="Rule removed" src="https://github.com/user-attachments/assets/f0d4e673-ecd5-4ff6-8cf7-46fc673361bc" />


Documentation of Commands Used (Linux)

      sudo ufw enable
      sudo ufw status
      sudo ufw deny 23
      sudo ufw allow 22
      sudo ufw delete deny 23
