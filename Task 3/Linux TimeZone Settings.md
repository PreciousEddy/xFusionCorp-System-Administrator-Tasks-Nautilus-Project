# Linux TimeZone Settings -xFusionCorps Industries

*During the daily standup, it was pointed out that the timezone across <Nautilus Application Servers> in <Stratos Datacenter> doesn't match with that of the local datacenter's timezone which is Australia/Lord_Howe*

This Readme provides an instruction how I corrected the timezone mismatch across <Nautilus Application Servers> in the <Stratos Datacenter>

## Logon the App servers and Switch to root Users

```ssh Chibuike@<app server1>```

After logging on switch to root user

```sudo su -```

## Identify the current timezone settings in server

First, verify the current timezone settings on the Nautilus Application Servers in the Stratos Datacenter. Using the command below:

```timedatectl```

## Set the TimeZone to Australia/Lord_Howe

Once you've identified that the current timezone is different from Australia/Lord_Howe, you need to update the timezone settings on all the servers to match the local datacenter's timezone. Using the command below:

```timedatectl set-timezone Australia/Lord_Howe```

## Verify the changes

After updating the timezone settings, it's essential to verify that the changes have been applied correctly. Using the command below

```timedatectl```



---
*Note: I had to do this all on all the Organization servers. Quick hack Using the ```timedatectl -h``` command,helps give syntax to set the time zone and many others*