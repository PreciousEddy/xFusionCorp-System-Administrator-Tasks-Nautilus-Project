# Create a Linux User with Non-Interactive Shell

This guide outlines the steps to manually create a new Linux user with a non-interactive shell. The non-interactive shell is commonly used for service accounts or accounts that do not require direct shell access.

## Step-by-Step Process

### 1. Log in to your Linux System

Log in to your Linux system with administrative privileges or as the root user.

```ssh@<User with administrative privileges```

### 2. Add the New User with Non-Interactive Shell

Use the `useradd` command to add a new user with a non-interactive shell. The `/usr/sbin/nologin` shell can be used to prevent the user from logging in directly.

``` sudo useradd -s /usr/sbin/nologin <username> ```

Replace <username> with the desired username for the new user.

### 3. Set the User's Password (If needed)

Use the 'passwd' command to set the password for the new user.

```sudo passwd <username> ```

Replace <username> with the username you created in the previous step. You will be prompted to enter and confirm the new password.

### 4. Optional: Add Additional Information (If Required)

If desired, you can add additional information for the user using the usermod command. For example, you can set the user's full name.

```sudo usermod -c "User's Full Name" <username> ```

Replace <username> with the username you created earlier and "User's Full Name" with the actual name.

### 5. Verify the User (Confirmation).

To ensure the user was created successfully, you can use the id command to check the user's details.

```id <username>```

Replace <username> with the username of the newly created user.

## Important Note.

Creating a user and setting passwords require administrative privileges. Always run the commands with sudo or as the root user.

## Example

Let's go through an example to create a new user named "Chibuike" with a non-interactive shell:

1. Log in to your Linux system with administrative privileges.

```ssh@PreciousEddy```

2. Add the new user with a non-interactive shell:

```sudo useradd -s /usr/sbin/nologin Chibuike```

3. Set the Chibuike's password:
   
   ```sudo passwd Chibuike```
   Enter and confirm the new password for Chibuike

4. Optionally add additional Information.
    
    ```sudo usermod -c "Example User" exampleuser```

5. Verify the user:

    ```id Chibuike```
   
   This will display the user <Chibuike> Information
   
---
*Note: Ensure you follow best security practices and exercise caution when granting shell access to users.*