<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDP, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create Windows and Linux(Ubuntu) Virtual Machines
- Initiate ping between machines
- Disable/Enable network traffic in Newtwork Security Group
- Using Wireshark observe ICMP / SSH / DHCP / DNS / RDP Traffic

<h2>Actions and Observations</h2>

<p>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/d3a2caf8-32fb-4e55-bd9d-3aba3e509b2e" height="60%" width="60%" alt="windowsandlinuxvm"/>
</p>
<p>
Created windows and linux VM with subset
</p>
<br />

<p>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/dcdca8c5-8ccf-48ac-93db-8c00e7d284d1" height="60%" width="60%" alt="filter icmp"/>
</p>
<p>
Downloaded and installed Wireshark on Windows 10 VM and filtered on ICMP to observe traffic.
</p>
<br />

<p>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/2736b469-23d8-4a96-adc2-27079b603621" height="60%" width="60%" alt="ping and observe icmp"/>
</p>
<p>
Using command prompt and private IP address, pinged Ubuntu VM and observed ICMP activity in Wireshark
</p>
<br />

<p>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/1e4ba16f-8239-433b-bb81-7b056e2c03b1" height="60%" width="60%" alt="ping and observe icmp"/>
</p>
<p>
Pinged www.google.com and observed ICMP activity in Wireshark
</p>
<br />

<p>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/0fb824d2-297b-4509-9091-1757c222fa57" height="60%" width="60%" alt="perpetual ping icmp"/>
</p>
<p>
Initiated ongoing ping of Ubuntu VM in Windows VM using Wireshark
</p>
<br />

<p>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/dc0862cb-2787-4373-86e9-08db71d53c19" height="60%" width="60%" alt="icmp disabled nsg"/><br>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/03eb4ed3-c6cd-4b04-856c-6b3ac065f792" height="30%" width="30%" alt="icmp cmd win10"/>
</p>
<p>
Disabled incoming (inbound) ICMP traffic in Ubuntu Network Security Group and observed command line in Windows VM
</p>
<br />

<p>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/b25120dd-8da2-4fb0-aa83-e1175b65a9b2" height="60%" width="60%" alt="icmp re-enabled"/>
</p>
<p>
Re-enabled incoming (inbound) ICMP traffic in Ubuntu Network Security Group and observed command line in Windows VM
</p>
<br />

<p>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/a7530415-b5d1-492e-b098-99e3c565575b" height="60%" width="60%" alt="observe ssh"/>
</p>
<p>
Filtered to SSH in Wireshark and observed via command prompt what happens when entering username and password for Ubuntu VM
</p>
<br />

<p>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/5f96bd86-0ce0-4881-8619-2d4e74146fd7" height="60%" width="60%" alt="observe dhcp"/>
</p>
<p>
Filtered to DHCP in Wireshark and observed what happens when trying to issue a new IP address to the VM
</p>
<br />

<p>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/73d5b44d-1851-40a1-a65b-9b3577ea8ee1" height="60%" width="60%" alt="observe dns1"/><br>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/7015067e-df96-47de-893b-ae51ccc26bed" height="60%" width="60%" alt="observe dns2"/>
</p>
<p>
Filtered to DNS in Wireshark and observed activity in Wireshark when performing nslookup on Google and Disney websites
</p>
<br />

<p>
<img src="https://github.com/krystalcherry/azure-network-protocols/assets/158524799/a0e976fc-f24e-48a6-8fce-ef355dadc98c" height="60%" width="60%" alt="observe RDP"/>
</p>
<p>
Filtered to RDP and observed that traffic is always being transmitted
</p>
<br />

