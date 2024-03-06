# Active Directory Virtual Lab

A virtual server environment connected with multiple PCs managed by Domain Controller.

Objectives:\
Simulate enterprise Active Directory environment using Hyper-V, join PCs into the domain, perform domain management tasks, manage users & computers and setup group policy.

virtlab-addc steps:
1.	Create a VM on Hyper-V
2.	Install Windows Server 2022
3.	Configure Windows Server 2022 (change PC-name, get current IP Address configured & set to static, set 127.0.0.1 as preferred DNS, set 8.8.8.8 as alternative DNS and restart the VM)
4.	Install Active Directory Domain Services
5.	Configure Active Directory Domain Services and create local Root Domain
6.	Create new user account, uncheck change password at next logon (bwayne)

virtlab-pc1 steps:
1.	Create a VM on Hyper-V
2.	Enable TPM
3.	Install Windows 11 Enterprise
4.	Configure Windows 11 Enterprise (change PC-name, set virtlab-addc IP Address as preferred DNS, set 8.8.8.8 as alternative DNS and restart the VM)
5.	Test if connection to the Root Domain is successful by using nslookup and ping command.

Demo:
1.	Create Organizational Units (OU) PH > Computers (Server, Workstations), Users (Accounting, HR, Engineering, Sales, Termed), Distribution Group, Security Group (Payroll, IT, Onboarding, Contracts, Sales)
2.	Create new users account (ckent)
3.	Move user to different OUs
4.	Create new groups IT (Domain Admins), Onboarding (HR New Hire), Payroll (Deposit)
5.	Add/remove user to a Group
6.	Find specific Computer, Groups, OU and Users
7.	Update computer description and user information
8.	Disable/Enable a user account and validate to login in virtlab-pc1
9.	Reset a user password and change user account password (bwayne) in virtlab-pc1
10.	Join virtlab-pc2 to the domain and verify that virtlab-pc2 has been added in Active Directory Computers
11.	Login as new user account (ckent) and change password
12.	Create Group Policy that prevents access to control panel and validate that control panel cannot be access

Details:\
VM name\
virtlab-addc

PC-Name\
virtlab-addc

Administrator\
Server2022

Root Domain\
virtlab.local

Directory Services Restore Mode (DSRM)\
Server2022DSRM

Burce Wayne(AD account)\
bwayne\
PW initialize - Password1\
PW reset - Newpassword1\
PW change - Lastpassword1

Clark Kent(AD account)\
ckent\
PW initilize - Password2\
PW change - Newpassword2

---
VM name\
virtlab-pc1

PC-Name\
virtlab-pc1

batman (local account)\
Password1

---
VM name\
virtlab-pc2

PC-Name\
virtlab-pc2

superman (local account)\
Password2

References:\
https://www.youtube.com/watch?v=F8AW-wG6prk \
https://www.youtube.com/watch?v=TN5DB-8eK9o \
https://www.youtube.com/watch?v=aqA6bktFHoY
