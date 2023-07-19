
# Automating Backup Process - xFusionCorp Industries

This README provides instructions for automating the backup process that was previously performed manually by the xFusionCorp Industries system admins team. To automate this task, the team has developed a new bash script named `xfusioncorp.sh`. 

## Granting Executable Permissions to xfusioncorp.sh

To ensure the successful automation of the backup process on App Server 1, the `xfusioncorp.sh` script must be executable, and every user on the system should have the ability to execute it.

Follow these steps to grant executable permissions to the script and allow all users to execute it:

### Step 1: Log in to App Server 1

Log in to App Server 1 with administrative privileges or as the root user.

```ssh Chibuike@<servername>```

### Step 2. Switch to the root user's shell environment

  ``` sudo su -```

  switch to the root user's shell environment with elevated privileges, effectively becoming the root user for the duration of that shell session.

### Step 3. List the File Existing persmission

  ```ls -ltr /tmp/xfusioncorp.sh```

This lists the existing file permission

### Step 4: Grant Executable Permissions

Run the following commands to give executable permissions to the `xfusioncorp.sh` script:

```chmod +x /tmp/xfusioncorp.sh```
```chmod a+x /tmp/xfusioncorp.sh```

### Step 5: Verify Permissions

To confirm that the permissions have been set correctly, run the following command:

```ls -lrt /tmp/xfusioncorp.sh```

The output should show that the script has the executable permission for all users.

## Running the Backup Automation Script

With the executable permissions granted to `xfusioncorp.sh`, the script is now ready to be executed by any user on App Server 1. To run the backup automation, simply use the following command:

```sh /tmp/xfusioncorp.sh```

The script will now run and automate the backup process as designed by the xFusionCorp Industries system admins team.

---
*Note: This README shows that the `xfusioncorp.sh` script performs the necessary backup tasks and automation. The content of the `xfusioncorp.sh` script itself is not provided in this document.😊*