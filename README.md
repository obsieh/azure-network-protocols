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

- Step 1: Create and Assign NSGs
- Step 2 : Configure NSG Rules
- Step 3 : Deploy and Connect Azure Virtual Machines
- Step 4 : Test and Inspect Traffic

<h2>Actions and Observations</h2>
Step 1: Configure NSGs

![image](https://github.com/user-attachments/assets/cc7b77c4-0769-44a4-a0b4-ef69f331e600)

</p>
<p>
Begin by creating Network Security Groups (NSGs) and attaching them to specific subnets or NICs of Azure Virtual Machines. Define inbound and outbound rules to control the flow of traffic based on port, protocol, or IP address. For example, you can allow HTTP traffic on port 80 while restricting other access. This step ensures only authorized traffic flows into or out of your network.
</p>
<br />
Step 2: Deploy VMs and Test Connectivity

![image](https://github.com/user-attachments/assets/82e83b75-c0b0-4e00-92e1-f8705ae2ba4a)

</p>
<p>
Set up two or more Azure Virtual Machines (VMs) within the same virtual network or across different subnets. Use tools like ping or telnet to test the connection between the VMs. This step helps verify if traffic is allowed or blocked based on the configured NSG rules, ensuring proper communication.
</p>
<br />
Step 3: Simulate Traffic Scenarios

![image](https://github.com/user-attachments/assets/4a4d4040-fafc-4699-bfa4-905800a27430)

</p>
<p>
Generate various traffic scenarios between the VMs, such as RDP, SSH, or HTTP traffic. Modify NSG rules to refine the control over what is allowed or denied. Observing whether traffic flows or gets blocked based on the scenario helps confirm that the rules are effectively managing access.
</p>
<br />
Step 4: Inspect Logs

![image](https://github.com/user-attachments/assets/d70298fd-7a6a-4319-9981-88bd4f727c90)

Enable NSG flow logs to capture details about the traffic passing through the NSGs. Use Azure Monitor or other tools to review these logs, checking for allowed and denied traffic. Analyzing the logs provides insights into rule performance and helps identify any misconfigurations or unexpected traffic patterns.
