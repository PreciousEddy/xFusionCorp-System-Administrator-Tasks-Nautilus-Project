# Create a custom Apache User named jim on the App server 3 in Stratos Datacenter

---

For security reasons the xFusionCorp Industries security team has decided to use custom Apache users for each web application hosted, rather than its default user. This will be the Apache user, so it shouldn't use the default home directory. Create the user as per requirements given below:

a. Create a user named jim on the App server 3 in Stratos Datacenter.

b. Set its UID to ```1803``` and home directory to ```/var/www/jim.```

---
## Requirements

* You must log in as root or another user with sudo privileges
* You must have access to the App server 3 in Stratos Datacenter

## Instructions:

1. Log on to the server <app server 3> and switch to sudo

   ```ssh chibuike@<app server 3>```
       ```sudo su -```

2. Run the following command to create the user:

    ```useradd jim -u 1803 -d /var/www/jim```

3. Run the following command to set the home directory:

    ```chown jim /var/www/jim```

4. Run the following command to add the user to the sudo group:

    ```add user jim sudo```

5. Once all is done, the user jim will be created with the following properties:
    * UID: 1803
    * Home directory: /var/www/jim
    * Shell: /bin/bash
    * Member of the sudo group

  *This user will be able to access the /var/www/jim directory and run sudo commands*