<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory and Domain Server Deployed in the Cloud (Azure)</h1>
This tutorial outlines the Creation of virtual machines, their deployment and testing of their connection within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create Virtual Machine
- Launch Virtual Machines
- Disable firewall
- Make Vertual Machine Domain 
- Test 

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="1710" alt="image" src="https://github.com/user-attachments/assets/eb934f01-70a7-4578-a81c-edadfb7359a3">

</p>
<p>
  For the sake of the lab I created 2 virtual machines. 1 to act as a computer and the other; the server it will connect to. When creating VM's the components of the machines will often be created automatically, but to make it so there is seamless interaction between the a (VM's) I created a (Resource Group) and (Virtual Network) that both Virtual machines will share. 
  My last step in this process was making one of my (VM's) a server and I did that by changing its private ip address from (Dynamic) to (Static) form within the network interface. Now I have 2 uniqe (VM's) to run simulations. (Client1 and DC-1)
  
</p>
<br />

<p>
https://www.youtube.com/watch?v=hEuB_JQrlN0

![A8D1C5A8-7C1C-4825-96D9-60E4BE1A3E1F](https://github.com/user-attachments/assets/d50060a8-800d-4504-8d96-387cd403ec91)


</p>
<p>
Now that the virtual machines are up and running I used their individual public ip addresses to log into both via remote desket. With both opened and (Domain Controller) accessible I disabled the firewall the make the domain reachable (run/wf.msc). Once the firewall is disabled I changed the the other (VM's) (DNS Server) to the private ip address of the Domain (VM). The virtual machines are now connected.
</p>
<br />

<p>
<img width="1710" alt="DA26B395-F1B6-4DA8-A4AF-AE53ED4BD5D1" src="https://github.com/user-attachments/assets/3799e604-5020-4fe4-975d-302aab6e92c4">

</p>
<p>
With everything in order I used (Powershell) I tested connectivity between the virtual machinees and verified that one is indeed the domain by using (ping)+ the domain private ip address. The connection is successful 
</p>
<br />
