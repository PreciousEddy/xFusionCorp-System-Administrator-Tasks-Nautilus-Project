# Create a group named ```nautilus_developers``` in all App servers in Stratos Datacenter and add the user ```rajesh ``` to the group

---
There are specific access levels for users defined by the xFusionCorp Industries system admin team. Rather than providing access levels to every individual user, the team has decided to create groups with required access levels and add users to that groups as needed. See the following requirements:

a. Create a group named nautilus_developers in all App servers in Stratos Datacenter.
b. Add the user rajesh to nautilus_developers group in all App servers. (create the user if doesn't exist).

---
## Requirements

* You must log in as root or another user with sudo privileges
* You must have access to the all App servers in Stratos Datacenter

---

## Instructions

1.  Log on to the server each <app server> and switch to sudo
    
    ```ssh chibuike@<app server 1>```
       ```sudo su -```

2.  Run the following command to create the group:

    ```groupadd nautilius_developers```

3.  To add the user to the group, use the following command:

    ```useradd -c "Rajesh Developer" -m rajesh```

4. Run the following commands to add the user to the group:

    ```usermod -aG nautilus_developers rajesh```

---
*Once you have run these commands, the nautilus_developers group will be created on all app servers in Stratos Datacenter and the User rajesh will be added to the group, if the user doesn't already exist.*

### N.B; You have to repeat these steps on all other App servers