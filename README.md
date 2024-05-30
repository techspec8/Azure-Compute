<p align="center">
<img src="https://i.imgur.com/tUjfXAc.png alt="Microsoft Azure Logo"/>
</p>

<h1>Creating Resource Groups and Virtual Machines in Azure</h1>
<b>This tutorial outlines the steps to creating virtual machines and connecting them to the same network security group in Azure.<b/>
<br />

<h2>Environments and Technologies Used</h2>

- Cloud Computing in Azure  
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Linux (Ubuntu)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create Resource Group 
- Configure Windows 10 Virtual Machine with Vnet and Subnet
- Configure Linux Virtual Machine and connect to VM1 Vnet
- Connect to Remote Desktop 
<br />
<p>
<img src= https://i.imgur.com/4XCsQoC.png
</p>
<br/>

<h2>Deployment and Configuration Steps</h2>

<b> Begin by naming your Resource Group RG-Lab2. Choose a region such as EAST US 2. Then, click 'Review and Create' to observe validation, then 'Create' to complete.   
</b>
<p>
<img src= https://i.imgur.com/fX1aTAX.png 
<p>
<img src= https://i.imgur.com/UQWExyF.png
</p>

<br />

<b> Next, connect your Virtual Machines to the Resource Group you created. You will name each Virtual Machine VM1 or VM2. Make sure to use the same region that your Resource Group was created in. Next, choose an operating system for your VM (e.g. Windows 10/LinuxUbuntu). Create a username/password, then check the 'Licensing' box. Click next until you get to 'Networking'. Here, you will create a Virtual Network, Subnet, and Public IP address, and notice that you are using inbound RDP Port 3389. Click 'Review + Create'. If validation passes, click 'Create'. Wait for the message 'Your deployment is complete' and refresh your page. If you go back and click on the 'Resource Group', you will now see your VM1 and the services you created.  
</b>

<p>
<img src= https://i.imgur.com/wwS8T8i.png
</p>
  
<p>
<img src= https://i.imgur.com/zFOyfJn.png
</p>
  
<b>Repeat the same steps to create VM2 except, choose the Linux (Ubuntu) operating system. Once you're in 'Networking', <b>connect to VM1's virtual network</b> by choosing VM1-vnet from the drop-down, your 'Subnet' will be the same as your VM1, and a new 'Public IP' will be assigned for VM2. Notice that you are now using inbound SSH Port 22. Wait for the message 'Your deployment is complete' and refresh your page.  
</b> 

<p>
<img src= https://i.imgur.com/8ofVEv2.png
</p>

<b>Back in Resource Group, sort by type, and observe that both Virtual Machines are on one virtual network/subnet.</b>
<p>
<img src= https://i.imgur.com/dLkMeG9.png
</p>
  
<br />

<b>Next, copy the Virtual Machine's Public IP address and access Remote Desktop from your start menu. Then, connect using the Username and Password you created in each Virtual Machine. If using a Mac OS, download the Microsoft Remote Desktop application (shown below) from the Apple Store to complete this lab.  </b>
<p><img src= https://i.imgur.com/yGH8lCB.png <p/>

<p><img src= https://i.imgur.com/QJJeNC4.png </p> <img src= https://i.imgur.com/vAbHgfC.png</p>  
<br/>
<b>You are now ready to observe network traffic between Virtual Machines using Wireshark and experiment with Network Security Groups and Inspecting Network Protocols here ->(https://github.com/techspec8/Network-and-Protocols/tree/main)</b>
