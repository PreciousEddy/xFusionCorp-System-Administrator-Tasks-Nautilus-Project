## Linux Archives
---
**Task Details:** 

*On Nautilus storage server in Stratos DC, there is a storage location named **/data**, which is used by different developers to keep their data (non confidential data). One of the developers named rose has raised a ticket and asked for a copy of their data present in **/data/rose** directory on storage server. **/home** is a FTP location on storage server itself where developers can download their data. Below are the instructions shared by the system admin team to accomplish this task.*

*a. Make a `rose.tar.gz` compressed archive of /**data/rose** directory and move the archive to /home directory on Storage Server*.

---
## Instructions:

- SSH into the Nautilus Storage Server.

   **`ssh username@storage-server-ip`**

- Navigate to the /data directory:

        ``cd /data``

- Use the tar command to create a compressed archive of the **rose** directory:

    **`tar -czvf rose.tar.gz rose/`**

 _This command creates a tarball (*rose.tar.gz)* of the rose directory._

- Move the **rose.tar.gz** file to the **/home** directory:

    **``mv rose.tar.gz /home/``**

---

## Accessing the Archive

The rose.tar.gz file is now available in the /home directory on the Nautilus Storage Server. You can download this file using your preferred FTP client.


