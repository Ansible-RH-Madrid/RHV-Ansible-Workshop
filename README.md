**
## RHV + Ansible Tower Workshop
**

We'll start by logging into the demo environment at: https://bit.ly/2LosqDT  
There, please input your email and code so that a Lab may be assigned to you.

|Activation Code:|rhlisboa|
|-|--|



Example:
![image](images/example_get_guid.png)


Section 1: Red Hat Virtualization Essentials
This first section aims to provide an overview of the Red Hat Virtualization Administration Portal and you’ll learn to:
Start existing virtual machines.
Create virtual machines. 
Access the console of a virtual machine.
Red Hat Virtualization Administration Portal
To access the Red Hat Virtualization Administration Portal, use the URL provided to you (eg. https://rhvm-?GUID?.rhpds.opentlc.com) and click on the link "Administration Portal".



When accessing the Administration Portal login page, use the following credentials (Profile=Internal):

|admin:|r3dh4t1!|
|-|--|


Example:
![image](images/login_rhv.png)  

<br />

First screen you’ll see is the main dashboard, which provides an overview of the environment, including information on Data Centers, Clusters, Hosts, Data Storage Domains and Virtual Machines.
On the left side of the screen you may access operations related to compute, network and storage.

Example:
![image](images/ui_overview.png)  

<br />

# Lab 1.1 - Explore the Administration Portal
Explore the Administration Portal, but don’t change configurations nor create virtual machines yet.
Virtual Machines View and Essential Operations
This environment already has some existing virtual machines, as you can notice when accessing Compute → Virtual Machines.

Next the instructor will give a brief overview and explanation of the UI.  
Please feel free to follow along or explore on your own, just as long as you don't create or destroy any objects it won't harm the learning curve.

<br />

# Lab 1.2 - Start Virtual Machine 
Using the vertical menu on the left, go to Compute → Virtual Machines.  
Click on the “database” virtual machine name to view its information.
Click on the “wordpress” virtual machine name to view its information.

Click on “Run” button to start the "database" virtual machine.
Click on “Run” button to start the "wordpress" virtual machine.

Click on “Console” to access the virtual machines console, to verify it started properly. Note that you won’t be logging into this virtual machine.

Close the console window when you confirm the virtual machines have started.  

<br />

# Lab 1.3 - Explore the User Admin Portal
RHV has a very handy "VM Portal” that when paired with RBAC, allows for the self-adminstration of VMs by the end-user, without accessing the more vital "Administration Portal".
Go back to the welcome screen by clicking the Red Hat logo in the top left corner.

Click on “VM Portal” link.
You'll be greeted with a view of your VMs (being full admin, this will be all VMs).  

Example:
![image](images/user_portal01.png) 


Click on the "database" VM to access the virtual machine self-management page. You'll be able to amongst others: access the virtual console, get an overview of resource consumption, effect power operations, etc.

Example:
![image](images/user_portal02.png)

Ok, let's get back to the "Admin Portal".

<br />

# Lab 1.3 - Live Migration of the "wordpress" Memory State and of the "database" Virtual Disk 
Let's start by conecting to the wordpress frontend: https://wordpress-GUID.rhpds.opentlc.com  
This will be used to atest availability during the live migration ops. Feel free to browse the site's interface while the following operations take place.

<br />

Using the vertical menu on the left, go to Compute → Virtual Machines.  
Click on the “wordpress” virtual machine row to select it. In the common VM operations, choose Migrate (it will automatically select the other available host).

Example:
![image](images/lv_select.png)  

<br />

Go ahead and click "Migrate"
![image](images/lv_vm02.png)  
You can check the progress of the migration either on the VMs view or the Tasks view.  

<br />

Now, please select the "database" VM, this time clicking on it's name and then accessing the "Disks" tab in order to live migrate the device.  
![image](images/lv_vm03.png)  
  
<br />

![image](images/lv_vm04.png)  
  
<br />

![image](images/lv_vm08.png) 

In the Tasks view you can now follow the progress of this operation.  

<br />

# Lab 1.4 - Create Virtual Machine 
Virtual machines can be created from templates or can have the operating system installed from its installation media. For the purpose of this lab, you’ll be creating a virtual machine from a template.  
Using the vertical menu on the left, go to Compute → Virtual Machines.
Click New to open the New Virtual Machine window.  

Considering this scenario, you’ll be creating a virtual machine with the following information:  
  

|-|--|
|-|--|
|Cluster:|Production|
|Template:|Rhel-7.5-demo base version(1) |
|Operating system:|Red Hat Enterprise Linux 7.x x64  |  
|Instance Type:|Small  |   
|Optimized for:|Server  |  
|Name:|test_vm  |  
|Description:|to_detete  |  
|-|--|


Check:   
Start in Pause Mode  
Delete Protection

For nic1, please select:  
vm public net/vm public net

Keep defaults for everything else.
Click OK.  

When the virtual machine creation finishes, click on Run button.
To access virtual machine console, click on Console button.
ℹ
For more details on all fields in the New Virtual Machine window, see Red Hat Virtualization documentation.
If you’d like to log into the virtual machine operating system, use the following credentials. 

Login: admin
Password: r3dh4t1!



