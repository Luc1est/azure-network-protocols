# azure-network-protocols<p align="center">
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

- Step 1- install a protocal analyzer/packet sniffer (wireshark).this will allow us to examine the activity thats happening on the network interface card. Basically this will let us see all the activity that is happening with our human eyes

- Step 2- Filter for ICMP traffic, this is what Ping uses to test connectivity between two devices. we do this because there is too much observable traffic, and if e dont filter it we could miss it with all the other data being sent.

- Step 3- Retrieve the private IP address of the Ubuntu VM (linux-vm) and attempt to ping it from within the Windows 10 VM

- Step 4

<h2>Actions and Observations</h2>


![image](https://github.com/user-attachments/assets/794a50c7-d95b-4dfb-b0ad-5910df7a02ac)
installing wireshark will allow us to see the Traffic/activity happening between our 2 VM's



![image](https://github.com/user-attachments/assets/d8776773-f684-4aa8-a46d-52c0e966ec5c)
go to the search bar and Type in ICMP, this will filter only PING Traffic and make it easier to find your end point connections, instead of trying to find a needle in a haystack with all the unfiltered Traffic.


![image](https://github.com/user-attachments/assets/7620901d-e6d4-4150-b8b4-bcae798a2135)
Head to your Linux VM that we already setup and copy the Private IP Address. once you have done this Open powershell.
