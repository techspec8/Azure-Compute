<p align="center">
<img src="https://i.imgur.com/tUjfXAc.png alt="Microsoft Azure Logo"/>
</p>

<h1>Creating Resource Groups and Virtual Machines in Azure</h1>
This tutorial outlines the steps to creating virtual machines and connecting them to the same network security group in Azure.<br />

<h2>Environments and Technologies Used</h2>

- Cloud Computing in Azure  
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Linux (Ubuntu)

<h2>High-Level Deployment and Configuration Steps</h2>

<p>
<img src= https://i.imgur.com/4XCsQoC.png
</p>
  
- Create Resource Group 
- Create Windows 10 Virtual Machine with Vnet and Subnet
- Create Linux Virtual Machine and connect to VM1 Vnet
- Install Wireshark in Windows VM
- Observe Traffic (ICMP, SSH, DHCP, DNS, RDP)
- Observe Commands Between Powershell and Wireshark

<h2>Deployment and Configuration Steps</h2>

<p> Begin by naming your resource group (e.g., RG-Lab2). Choose a region (e.g., EAST US 2). Click 'Review and Create' observe validation, then click 'Create'.   
</p>
<p>
<img src= https://i.imgur.com/fX1aTAX.png 
<p>
<img src= https://i.imgur.com/UQWExyF.png
</p>

<br />

<p> Next create your virtual machines and connect them to the resource group that you just created. You will name each virtual machine (e.g. VM1 or VM2). Make sure to use the same region that your resource group was created in. Next, choose an operatng system for your VM (e.g. Windows 10/Ubuntu). Create a user name/password, then check the 'Licensing' box. Click next until you get to 'Networking'. Here, you will be creating a Virtual Network, Subnet, Public IP address, and notice that you are using inbound RDP Port 3389. Click 'Review + Create'. If validation passes, click 'Create'. Wait for the message 'Your deployment is complete' and then refresh your page. If you go back and click on the 'Resource Group', you will now see your VM1 and services that you created.  
</p>

<p>
<img src= https://i.imgur.com/wwS8T8i.png
</p>
  
<p>
<img src= https://i.imgur.com/zFOyfJn.png
</p>
  
<p>Repeat the same steps to create VM2 except, choose the Linux (Ubuntu) operating system. Once you're in 'Networking', <b>connect to VM1's virtual network</b> by choosing VM1-vnet from the drop-down, your 'Subnet' will be the same as your VM1 and a new 'Public IP' will be assigned for VM2. Notice that you are now using inbound SSH Port 22. Wait for the message 'Your deployment is complete' and then refresh your page.  
</p> 

<p>
<img src= https://i.imgur.com/8ofVEv2.png
</p>

<p>If you click back into your resource group, sort by type, you will now see both virtual machines and one virtual network. Next we observe various network traffic to and from VM1 and VM2 with Wireshark as well as experiment with Network Security Groups.</p>
<p>
<img src= https://i.imgur.com/dLkMeG9.png
</p>
  
<br />
