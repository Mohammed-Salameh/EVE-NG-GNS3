This guide provides a step-by-step process on how to upload appliance files to your EVE-NG instance using FileZilla, a popular FTP client. Uploading appliances allows you to add new devices and tools to your EVE-NG environment, expanding your network simulation capabilities.

## Prerequisites

- Ensure you have EVE-NG installed and accessible.
  
[Github For Appliances Repo](https://github.com/hegdepavankumar/Cisco-Images-for-GNS3-and-EVE-NG?tab=readme-ov-file).

[All Appliances](https://labhub.eu.org/UNETLAB%20II/addons/qemu/).

- Download and install FileZilla Client from [FileZilla's website](https://filezilla-project.org/).
- Obtain the appliance file(s) you wish to upload.

## Step-by-Step Guide

### Step 1: Connect to EVE-NG Using FileZilla

1. Open FileZilla Client.
2. In the top bar, input the following details:
   - **Host:** The IP address of your EVE-NG server.
   - **Username:** Your EVE-NG username (e.g., `root`).
   - **Password:** The password for your EVE-NG account.
   - **Port:** Typically, `22` for an SFTP connection.
3. Click `Quickconnect` to establish a connection to your EVE-NG server.

### Step 2: Navigate to the Correct Directory

Once connected, you need to navigate to the appropriate directory where appliance files should be uploaded.

1. On the right side of FileZilla (Remote site), navigate to the `/opt/unetlab/addons/qemu/` directory.
2. Inside this directory, you will find or need to create a subdirectory for your specific appliance. The name of the subdirectory should match the appliance name.

### Step 3: Upload Appliance Files

1. Locate the appliance file(s) on your local machine in FileZilla's left window pane (Local site).
2. Drag and drop the file(s) from the local site (your computer) to the remote site (EVE-NG server) into the correct appliance directory.

### Step 4: Set Correct Permissions

After uploading the files, you need to set the correct permissions for them.

1. Right-click on the uploaded file(s) in the remote site pane.
2. Select `File permissions...`.
3. Set the numeric value to `755` to ensure the EVE-NG can execute the appliance files.
4. Click `OK` to apply the permissions.

### Step 5: Verify the Appliance in EVE-NG

1. Log in to your EVE-NG web interface.
2. Create a new lab or edit an existing one.
3. Try to add a new node; the uploaded appliance should now be available in the list of devices.

## Troubleshooting

- **Connection Issues:** Ensure your EVE-NG server's IP address is correct and that it's accessible from your network. Verify that the SFTP port (22) is not blocked by your firewall.
- **Permission Errors:** If EVE-NG can't access the appliance, ensure you've set the permissions correctly to `755`.
- **Appliance Not Showing:** Double-check that you've uploaded the files to the correct directory and that the directory name matches the appliance name.

For further assistance, refer to the EVE-NG community forums or the official documentation.

---

This guide aims to simplify the process of uploading appliances to your EVE-NG environment using FileZilla, enhancing your network emulation experience.
