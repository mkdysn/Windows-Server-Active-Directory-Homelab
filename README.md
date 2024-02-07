# A Active Directory environment connected with multiple PCs

Active Directory Virtual Lab

Objectives:
1.	Install Windows Server 2022
2.	Install Windows 11 Enterprise PCs
3.	Install and configure Active Directory Domain Services
4.	Manage Active Directory Users & Computer
5.	Manage Active Directory Group Policy

homelab-addc steps:

1.	Create a VM on Hyper-V
2.	Install Windows Server 2022
3.	Configure Windows Server 2022 (change PC-name, get IP Address & set to static, set 127.0.0.1 as preferred DNS & 8.8.8.8 as alternative DNS and restart the VM)
4.	Install Active Directory Domain Services
5.	Configure Active Directory Domain Services and create local Root Domain
6.	Create Organizational Units (OU), Users, and Groups
7.	Move user to different OUs
8.	Find specific Computer, Groups, OU and Users
9.	Update computer description, user information and other details
10.	Add/remove user to a Group
11.	Disable/Enable a user account
12.	Reset a user password
13.	Proceed to homelab-pc1 step 1-7, verify that homelab-pc1 has been added in Active Directory Computers
14.	Create new user account (alexdgreat) and proceed to homelab-pc1 step 8-9.
15.	Create Group Policy that prevents access to control panel and proceed to homelab-pc1 step 10

homelab-pc1 steps:
1.	Create a VM on Hyper-V
2.	Enable TPM
3.	Install Windows 11 Enterprise
4.	Configure Windows 11 Enterprise (change PC-name, set homelab-addc IP Address as preferred DNS, set 8.8.8.8 as alternative DNS and restart the VM)
5.	Test if connection to the Root Domain is successful by using nslookup and ping command.
6.	Join homelab-pc1 to the domain
7.	Login as administrator and go back to homelab-addc step 13 to verify
8.	Login as new user account (alexdgreat)
9.	Change user account password (alexdgreat) and go back to homelab-addc step 15
10.	Validate if control panel cannot be access

Details:

VM name\
homelab-addc

Administrator\
Server2022

PC-Name\
homelab-addc

Root Domain\
homelab.local

Directory Services Restore Mode (DSRM)\
Server2022DSRM

alexdgreat\
Password1\
Newpassword1\
Lastpassword1

socdphilo\
Password1\
Newpassword2

--------------------------------------

VM name\
homelab-pc1

bernard (local account)\
Password1

PC-Name\
homelab-pc1

--------------------------------------
VM name\
homelab-pc2

robert (local account)\
Password2

PC-Name\
homelab-pc2


References:\
https://www.youtube.com/watch?v=F8AW-wG6prk \
https://www.youtube.com/watch?v=TN5DB-8eK9o \
https://www.youtube.com/watch?v=aqA6bktFHoY
