# azure-network-protocols
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

- Create our Resources
- Observe ICMP Traffic
- Observe SSH Traffic
- Observe DHCP Traffic

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/r9KSadx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a Resource Group and a Windows 10 Virtual Machine. Next Create a Linux (Ubuntu) and Observe Your Virtual Network within Network Watcher. 

</p>
<br />

<p>
<img src="https://i.imgur.com/RuMWbtj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Use Remote Desktop to connect to your Windows 10 Virtual Machine and Within your Windows 10 Virtual Machine Install Wireshark. Next Open Wireshark and filter for ICMP traffic only. Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM and observe ping requests and replies within WireShark.

</p>
<br />

<p>
<img src="https://i.imgur.com/bmiqFU6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Using Wireshark, filter for SSH traffic only. From your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address).Next filter for DHCP traffic only. From your Windows 10 VM, attempt to issue your VM a new IP address from the command line (ipconfig /renew) and Observe the DHCP traffic appearing in WireShark


</p>
<br />
