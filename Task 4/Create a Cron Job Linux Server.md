# Create a Cron Job Linux Server - xFusion corps

*The Nautilus system admins team has prepared scripts to automate several day-to-day tasks. They want them to be deployed on all app servers in Stratos DC on a set schedule. Before that they need to test similar functionality with a sample cron job. Therefore, I was tasked perform the steps below:*

*a. Install cronie package on all Nautilus app servers and start crond service.*

*b. Add a cron */5 * * * * echo hello > /tmp/cron_text for root user.*

## Logon the App Servers

```ssh Chibuike@<app server1>```

After logging on switch to root user

```sudo su -```

## Install cronie package and start crond service

Update the package list to ensure you have the latest information about available packages and Install cronie:

```sudo yum update```
Install the cronie package:
```sudo yum install cronie```

Start the crond service and enable it to start automatically on boot:

```sudo systemctl start crond.service```
```sudo systemctl enable crond.service```
```sudo systemctl status crond.service```

## Create a CronJob as per the task for root user

Open the cron table for the root user in edit mode using the crontab command:


```crontab -e``````

If prompted to select an editor, choose your preferred editor (e.g., nano, vim, etc.).

Add the following line to the cron table to run the command "echo hello > /tmp/cron_text" every 5 minutes:

```*/5 * * * * echo hello > /tmp/cron_text```

Save and exit the editor. For example, if you are using nano, press "Ctrl + X," then "Y" to confirm and "Enter" to save the changes.

## Check Cron Job for User root

```crontab -l```

To check for the Cron Job for User root

## Validate the ```cron_tab``` file

Validate the ```cron-text``` file is created sucessfully.

```ll /tmp/```

---
*I made sure to repeat these steps on each Nautilus app server to ensure the cron job is scheduled and running on all servers.*






