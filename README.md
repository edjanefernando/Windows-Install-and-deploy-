# Windows Server AD
- Type of Challenge: Learning
- Duration: 4 days
- Deadline: 26/04/2024
- Team challenge : solo

# System Preparation:
Set up your virtualization environment with Microsoft Hyper-V, VMware Workstation, or VirtualBox.
Download Windows Server 2022 evaluation.
Create VMs for Server, Domain Controller, and Client (if resources allow).
Install Windows Server 2022 on the Server and Domain Controller VMs.

- Start your VirtualBox and ensure that your Domain Controller VM is powered on.
Log in to the Domain Controller VM with administrative privileges.
Open the Server Manager:
Click on the "Start" menu.
Type "Server Manager" and press Enter.
In Server Manager, click on "Manage" from the top menu, then select "Add Roles and Features."
Follow the wizard, selecting "Active Directory Domain Services" as the role to install.
Once the role installation is complete, a notification will appear. Click on "Promote this server to a domain controller."
In the Deployment Configuration section, select "Add a new forest" and enter your desired domain name.
Set the Forest and Domain functional levels according to your requirements.
Configure the Directory Services Restore Mode (DSRM) password.
Review the DNS Options and ensure that DNS Server is checked. Enter the Directory Services Restore Mode (DSRM) password.
Click "Next" and proceed through the wizard. Review the options and click "Install" to promote the server to a domain controller.

- Create a New Active Directory Forest and Domain Structure:
Once the promotion process is complete, the server will restart.
Log back in to the Domain Controller VM.
Open Server Manager, navigate to "Tools" > "Active Directory Users and Computers."
Right-click on the "Domain" node and select "New" > "Organizational Unit."
Create organizational units (OUs) for user and group management according to your organizational structure.

- Configure DNS Service on the Domain Controller VM:
Open Server Manager.
Navigate to "Tools" > "DNS Manager."
Right-click on the server name and select "Configure a DNS Server."
Follow the wizard to configure DNS settings. You can choose the default settings unless you have specific requirements.
Once configured, DNS will be running on your Domain Controller.

- Join the Server VM and Client VMs to the Domain:
Start your Server VM and Client VMs in VirtualBox.
Log in to each VM using administrative credentials.
Open the "Control Panel" and navigate to "System and Security" > "System."
Click on "Change settings" next to "Computer name, domain, and workgroup settings."
Select "Change" and then choose the "Domain" option.
Enter the domain name that you configured earlier in the Domain Controller setup wizard.
You will be prompted to enter credentials for adding the computer to the domain. Enter the username and password of a domain administrator.
Follow the wizard to join the Server VM and Client VMs to the domain.
After completing these steps, you will have successfully set up Active Directory in VirtualBox, including promoting a Domain Controller, creating a new forest and domain structure, configuring DNS services, and joining Server and Client VMs to the domain.
