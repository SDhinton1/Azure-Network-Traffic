<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- 1:Install Windows 10 VM and Linux Ubuntu VM and observe their private ip Addresses.
- 2:In the Windows 10 VM Download WireShark and observe the traffic in the app.
- 3:Log into Linux and filter for ssh traffic in WireShark.
- 4:Observe different traffic names such as ICMP,SSH,DHCP,DNS, and RDP.

<h2>Actions and Observations</h2>

<p>
<img src="blob:chrome-untrusted://media-app/60b0281e-3d73-46f0-9ccd-23ff06875362" alt="Screenshot 2023-09-07 12.34.17 PM.png"/>![image](https://github.com/SDhinton1/Azure-Network-Traffic/assets/143854836/46e65163-4464-4094-a526-b693c37a2a80)
</p>
<p>
Download wireShark and observe the traffic that is running in the app.
</p>
<br />

<p>
<img src="blob:chrome-untrusted://media-app/68f524bc-b298-4e09-80d8-9c555c048d83" alt="Screenshot 2023-09-07 12.47.39 PM.png"/>![image](https://github.com/SDhinton1/Azure-Network-Traffic/assets/143854836/6cc1fa38-2967-493f-8b45-05ea86aec338)
</p>
<p>
In Powershell use the command ipconfig /renew to observe the traffic.
</p>
<br />

<p>
<img src="blob:chrome-untrusted://media-app/91160f8a-8391-4759-8f7c-99534763ff8f" alt="Screenshot 2023-09-07 12.51.49 PM.png"/>![image](https://github.com/SDhinton1/Azure-Network-Traffic/assets/143854836/d4088798-d25a-4124-b179-4c27e7556965)
</p>
<p>
Back in WireShark type tcp.port==3389 into the line and observe the traffic notice the traffic never stops this happens due to RDP showing a livestream of one computer to the other.
</p>
<br />
