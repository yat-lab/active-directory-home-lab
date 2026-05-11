# Windows Server 2022 VM Setup

## Environment
- VMware Workstation Pro 25H2
- Windows Server 2022 Standard Evaluation (Desktop Experience)
- Windows 10 Pro (client)

## DC01 Configuration
- VM Name: DC01
- OS: Windows Server 2022 Standard Evaluation (Desktop Experience)
- Hypervisor: VMware Workstation Pro 25H2
- RAM: 2 GB
- CPU: 2 cores
- Disk: 60 GB
- Network Adapter: NAT

# CLIENT01 Configuration
- VM Name: CLIENT01
- OS: Windows 10 Pro
- Hypervisor: VMware Workstation Pro 25H2
- RAM: 2 GB
- CPU: 2 cores
- Disk: 60 GB
- Network Adapter: NAT


### DC01 Installation Steps
1. Downloaded Windows Server 2022 Evaluation ISO from Microsoft
2. Created a new VMware virtual machine
3. Attached Windows Server 2022 ISO manually
4. Installed Windows Server 2022 Standard Evaluation (Desktop Experience)
5. Configured Administrator account password
6. Logged into Server Manager successfully
7. Configured static IPv4 address
8. Installed Active Directory Domain Services (AD DS)
9. Promoted DC01 to a Domain Controller
10. Created a new forest and domain:
    - yatlab.local
11. Installed and configured DNS automatically during AD DS promotion

## Windows 10 Client VM Installation

### CLIENT01 Installation Steps
1. Downloaded Windows 10 ISO using Microsoft's Media Creation Tool
2. Created a new VMware virtual machine for CLIENT01
3. Selected Windows 10 Pro as the guest operating system
4. Configured VM resources:
   - 2 GB RAM
   - 2 CPU cores
   - 60 GB virtual disk
5. Attached the Windows 10 ISO manually
6. Installed Windows 10 Pro
7. Created a local administrator account
8. Configured network settings manually


# Networking
- Both VMs use VMware NAT networking
- Static IPv4 addresses configured manually
- CLIENT01 and DC01 configured on the same subne

## Concepts Learned
- Difference between Organizational Units and Security Groups
- Domain Controllers centrally manage authentication
- Active Directory relies heavily on DNS
- Security Groups are used for permission assignment
- OUs are used for organization and Group Policy management

## Troubleshooting
- Initial VM failed to boot from ISO
- VMware showed EFI network timeout during boot
- Resolved installation issue by recreating VM and manually attaching ISO
- Encountered Windows setup license error during Easy Install
- Resolved issue by selecting manual OS installation method

## Goal
This VM will serve as the Domain Controller for the Active Directory home lab environment.