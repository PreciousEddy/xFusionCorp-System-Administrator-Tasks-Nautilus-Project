# Linux Add A User Without a Home Directory

---
The system admins team of xFusionCorp Industries has set up a new tool on all app servers, as they have a requirement to create a service user account that will be used by that tool.

Create a user named ```yousuf```  in ```App Server 2``` without a home directory.

##
* You must log in as root or another user with sudo privileges
* You must have access to the App server 2 in Stratos Datacenter

## Instructions:

1. Log on to the server <app server 2> and switch to sudo

   ```ssh chibuike@<app server 2>```

       ```sudo su -```

2. Run the following command to create the user without a Home directory:
    
     ```useradd -M yousuf```

     *The ```-M```   flag tells the   ```useradd```   command to not create a home directory for the user.*

---
😊