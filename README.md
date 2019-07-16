**
## Welcome all to this RHV + Ansible Tower Workshop

**
We'll start by logging into the demo environment at: https://bit.ly/2LosqDT

There, please input your email and code so that a Lab may be assigned to you.
|Activation Code:|rhlisboa|
|-|--|



Section 1: Red Hat Virtualization Essentials
This first section aims to provide an overview of the Red Hat Virtualization Administration Portal and you’ll learn to:
Start existing virtual machines.
Create virtual machines. 
Access the console of a virtual machine.
Red Hat Virtualization Administration Portal
To access the Red Hat Virtualization Administration Portal, use the URL provided to you (eg. https://rhvm-<GUID>.rhpds.opentlc.com) and click on the link Administration Portal.



When accessing the Administration Portal login page, use the following credentials:
Login
admin

Password
r3dh4t1!

Profile
internal


First screen you’ll see is the main dashboard, which provides an overview of the environment, including information on Data Centers, Clusters, Hosts, Data Storage Domains and Virtual Machines.

On the left side of the screen you may access operations related to compute, network and storage.

 Lab 1.1 - Explore the Administration Portal
Explore the Administration Portal, but don’t change configurations nor create virtual machines yet.
Virtual Machines View and Essential Operations
This environment already has some existing virtual machines, as you can notice when accessing Compute → Virtual Machines.


In order to execute some of the tasks in this Test Drive, the virtual machine named “dhcp” must be running and it’ll be started in the next lab. 

Lab 1.2 - Start Virtual Machine 
Using the vertical menu on the left, go to Compute → Virtual Machines.
Click on “dhcp” virtual machine name to view its information.

Click on “Run” button to start “dhcp” virtual machine.

Click on “Console” to access virtual machine console, to verify it started properly. Note that you won’t be logging into this virtual machine.

Close the console window when you confirm the dhcp virtual machine started.

Lab 1.3 - Create Virtual Machine 
Virtual machines can be created from templates or can have the operating system installed from its installation media. For the purpose of this lab, you’ll be creating a virtual machine from a template.
Considering this scenario, you’ll be creating a virtual machine with the following information:
Cluster
Production
Template
Rhel-7.5-demo | base version(1)
Operating system
Red Hat Enterprise Linux 7.x x64
Instance Type
Custom
Optimized for
Server
Name
vm-1
Description


Comment


Stateless


Start in Pause Mode


Delete Protection


nic1
vm public net/vm public net


Using the vertical menu on the left, go to Compute → Virtual Machines.
Click New to open the New Virtual Machine window.

Select “rhel-7.5-demo” Template.
Enter “vm-1” as Name for the virtual machine.
Keep defaults for everything else.

Click OK.
When the virtual machine creation finishes, click on Run button.
To access virtual machine console, click on Console button.
ℹ
For more details on all fields in the New Virtual Machine window, see Red Hat Virtualization documentation.
If you’d like to log into the virtual machine operating system, use the following credentials. 

Login
admin
Password
r3dh4t1!



