# Windows Server 2022 VM Setup

## Environment
- VMware Workstation Pro 25H2
- Windows Server 2022 Standard Evaluation (Desktop Experience)

## DC01 Configuration
- VM Name: DC01
- OS: Windows Server 2022 Standard Evaluation (Desktop Experience)
- Hypervisor: VMware Workstation Pro 25H2
- RAM: 2 GB
- CPU: 2 cores
- Disk: 60 GB
- Network: NAT
- Static IP: 192.168.x.x

## Installation Steps
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

## Active Directory Structure

    ## Organizational Units (OUs)
    - IT
    - HR
    - Servers
        ## Users
        - Thomas Yip

        ## Security Groups
        - IT_Admins

## Networking
- Adapter Type: NAT
- DNS Server: DC01
- Static IP configured manually through IPv4 settings

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