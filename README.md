# Active-Directory-

This lab consist of Windows Server 2019 - Configured as Domain Controller 1 (DC01) and a Windows 11 Pro host. Both Operating Systems will be installed onto Virtual Machines within VMware Workstation Pro.

### The goals of this lab were: 
1 - Deploy a Windows Server 2019 as a virtual machine with the following parameters:
  * PC name: "DC01"
  * Static IP: 192.168.50.5
  * DNS Server: 192.168.50.5 (Self)
  * Configure as Domain Controller
  * Active Directory installation

2 - Deploy a Windows 11 Pro as a virtual machine with the following parameters:
  * PC name: "Workstation1"
  * Local user account: "administrator"
  * Static IP: 192.168.50.50
  * DNS Server: 192.168.50.5
  * Joined to domain + verification using command line

3 - Configure Active Directory and create the following users
  * "ITadmin" 
  * "Eric"
  * "ServiceDesk"
  Verify these accounts can be logged into from "Workstation1" host PC.

### Lab Topology 

Device | OS | Hostname | IP Address |
***************************************
Domain Controller | Windows Server 2019 | DC01 | 192.168.50.5
Client | Windows 11 Pro | Workstation1 | 192.168.50.50





