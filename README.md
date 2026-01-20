# Active Directory Lab - Eric Harris
This lab consists of a virtualized Windows Server 2019 - Configured as Domain Controller 1 (DC01) and a virtualized Windows 11 Pro host. Both Operating Systems will be installed onto Virtual Machines within VMware Workstation Pro to simulate a small enterprise environment.
# Technologies Used:
* VMware Workstation Pro
* Windows Server 2019
* Windows 11 Pro
* Active Directory Domain Services
* DNS
* Group Policy Objects (GPO)
  
# Tasks
1. Deploy a Windows Server 2019 virtual machine configured as a Domain Controller with the following parameters:
   - Hostname: **DC01**
   - Static IP Address: **192.168.50.5/24**
   - DNS Server: **192.168.50.5 (Self)**
   - Active Directory Domain Services installed and configured

2. Deploy a Windows 11 Pro virtual machine with the following parameters:
   - Hostname: **Workstation1**
   - Local administrator account configured
   - Static IP Address: **192.168.50.50/24**
   - DNS Server: **192.168.50.5**
   - Successfully joined to the Active Directory domain and verified using command-line tools

3. Configure Active Directory user accounts:
   - **ITadmin**
   - **John**
   - **ServiceDesk**
   - Verified that all domain users were able to authenticate and log in to **Workstation1**

4. Configure Active Directory Group Policy:
   - Create an OU named **ITOffice**
   - Create an OU named **Users (OU)** 
   - Assign users **ITadmin** and **ServiceDesk** to the **ITOffice** group
   - Assign user **John** to the **Users** group
   - Create and apply a Group Policy Object to enforce a standardized desktop background

# Lab Topology 

Device | OS | Hostname | IP Address |

Domain Controller | Windows Server 2019 | DC01 | 192.168.50.5/24

Client | Windows 11 Pro | Workstation1 | 192.168.50.50/24

# Documentation
Documentation and step by step instructions can be found in the /docs directory.




