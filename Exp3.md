# Password Capturing Using Wireshark

## Aim

The aim of this experiment is to capture and analyze network packets using Wireshark in order to identify and extract passwords that are transmitted in plaintext over an unsecured network.

## Description

Wireshark is a powerful network protocol analyzer that enables monitoring and capturing of live network traffic. It provides detailed insights into the data packets transmitted across a network. This experiment demonstrates how insecure communication protocols such as HTTP, FTP, and Telnet transmit sensitive information like usernames and passwords without encryption, making them vulnerable to interception. Through this, the importance of using secure protocols such as HTTPS, SSH, and TLS can be understood.

## Procedure

1. Install and open Wireshark on the system.
![alt text](<Screenshots/Ex3-ss/Screenshot 2025-09-03 002729.png>)

2. Select the active network interface, either Wi-Fi or Ethernet, to begin capturing live packets.
![alt text](<Screenshots/Ex3-ss/Screenshot 2025-09-03 002736.png>)

3. Start a capture session and apply specific filters such as `http`, `ftp`, or `telnet` to monitor traffic related to login activities.
![alt text](<Screenshots/Ex3-ss/Screenshot 2025-09-03 002752.png>)

4. Visit a sample ip address and start capturing the packets.
![alt text](<Screenshots/Ex3-ss/Screenshot 2025-09-03 002823.png>)

5. After completing the ip address capturing, stop the packet capturing process.
![alt text](<Screenshots/Ex3-ss/Screenshot 2025-09-03 002858.png>)

6. Examine the captured packets using the search and analysis tools in Wireshark. Inspect ip address, port number filter commands.
![alt text](<Screenshots/Ex3-ss/Screenshot 2025-09-03 003006.png>)

7. Identify the sorted packets and look for any unusual packets.
[text](Exp3.md) ![text](<Screenshots/Ex3-ss/Screenshot 2025-09-03 003036.png>)


## Result

From this experiment, Wireshark captured live packets from the selected interface. Using filters, traffic related to the sample IP address was analyzed. Source/destination IPs, ports, and protocols were identified, and unusual packets were detected, showing how Wireshark helps monitor and analyze network traffic.
