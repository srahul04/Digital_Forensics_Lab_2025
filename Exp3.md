# Password Capturing Using Wireshark

## Aim
The aim of this experiment is to capture and analyze network packets using Wireshark in order to identify and extract passwords that are transmitted in plaintext over an unsecured network.

## Description
Wireshark is a powerful network protocol analyzer that enables monitoring and capturing of live network traffic. It provides detailed insights into the data packets transmitted across a network. This experiment demonstrates how insecure communication protocols such as HTTP, FTP, and Telnet transmit sensitive information like usernames and passwords without encryption, making them vulnerable to interception. Through this, the importance of using secure protocols such as HTTPS, SSH, and TLS can be understood.

## Procedure
1. Install and open Wireshark on the system.
2. Select the active network interface, either Wi-Fi or Ethernet, to begin capturing live packets.
3. Start a capture session and apply specific filters such as `http`, `ftp`, or `telnet` to monitor traffic related to login activities.
4. Visit a sample insecure login page using HTTP, and enter a test username and password for the purpose of analysis.
5. After completing the login attempt, stop the packet capturing process.
6. Examine the captured packets using the search and analysis tools in Wireshark. Inspect HTTP POST requests or FTP/Telnet authentication commands.
7. Identify the test username and password in plaintext within the packet details, confirming that insecure protocols expose sensitive information.

## Result
From this experiment, it was observed that Wireshark successfully captured packets containing login credentials when transmitted over insecure communication protocols. The test clearly showed that plaintext passwords could be intercepted, highlighting the vulnerability of using unencrypted services. Hence, the result emphasizes the necessity of using secure communication methods such as HTTPS, SFTP, and SSH to protect user credentials from unauthorized access.
