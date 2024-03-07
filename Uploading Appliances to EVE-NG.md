This guide provides a step-by-step process on how to upload appliance files to your EVE-NG instance using FileZilla, a popular FTP client. Uploading appliances allows you to add new devices and tools to your EVE-NG environment, expanding your network simulation capabilities.

## Prerequisites

- Ensure you have EVE-NG installed and accessible.
- Download and install FileZilla Client from [FileZilla's website](https://filezilla-project.org/).
- Obtain the appliance file(s) you wish to upload from the below links.

1. [Github For Appliances Repo](https://github.com/hegdepavankumar/Cisco-Images-for-GNS3-and-EVE-NG?tab=readme-ov-file).

2. [All Appliances](https://labhub.eu.org/UNETLAB%20II/addons/qemu/).

### Step 1: Connect to EVE-NG Using FileZilla

1. Open FileZilla Client.

![image](https://github.com/Mohammed-Salameh/Network-emulators/assets/140098574/a006f92e-f972-4498-bc20-6ca3b1da6d75)

2. In the top bar, input the following details:
   - **Host:** The IP address of your EVE-NG server.
   - **Username:** Your EVE-NG username (e.g., `root`).
   - **Password:** The password for your EVE-NG account.
   - **Port:** Typically, `22` for an SFTP connection.
3. Click `Quickconnect` to establish a connection to your EVE-NG server.

![image](https://github.com/Mohammed-Salameh/Network-emulators/assets/140098574/5be3586b-8517-4932-aae1-7fdac23e4ec2)


### Step 2: Navigate to the Correct Directory

Once connected, you need to navigate to the appropriate directory where appliance files should be uploaded.

1. On the right side of FileZilla (Remote site), navigate to the `/opt/unetlab/addons/qemu/` directory.

![image](https://github.com/Mohammed-Salameh/Network-emulators/assets/140098574/b415d9d5-2bb8-403e-9d2a-7e8988ab178a)

2. Inside this directory, you will find or need to create a subdirectory for your specific appliance. The name of the subdirectory should match the appliance name.

![image](https://github.com/Mohammed-Salameh/Network-emulators/assets/140098574/25fc08f6-e381-42ec-840e-6d3e863932bb)

### Step 3: Upload Appliance Files

1. Locate the appliance file(s) on your local machine in FileZilla's left window pane (Local site).

![image](https://github.com/Mohammed-Salameh/Network-emulators/assets/140098574/4e89afa7-86bf-4524-a5b9-0b4622482cd3)


2. Drag and drop the file(s) from the local site (your computer) to the remote site (EVE-NG server) into the correct appliance directory.

![image](https://github.com/Mohammed-Salameh/Network-emulators/assets/140098574/09b268ab-005c-441b-9f71-d009ff7d925e)

### Step 4: Verify the Appliance in EVE-NG

1. Log in to your EVE-NG web interface.

![image](https://github.com/Mohammed-Salameh/Network-emulators/assets/140098574/a05017cc-045c-43ba-ae44-dbb82a89edb7)

2. Create a new lab or edit an existing one.

![image](https://github.com/Mohammed-Salameh/Network-emulators/assets/140098574/0a7607ca-ea7b-487c-85a0-c47f0db13686)

3. Try to add a new node; the uploaded appliance should now be available in the list of devices.

![image](https://github.com/Mohammed-Salameh/Network-emulators/assets/140098574/587d180b-c4b2-4f98-8288-927971660c4b)

![image](https://github.com/Mohammed-Salameh/Network-emulators/assets/140098574/0ea0a10e-6a75-49b8-b5a7-a5ee41cb56c5)

![image](https://github.com/Mohammed-Salameh/Network-emulators/assets/140098574/cc4b8a1f-ef8f-4859-86e7-50c1c1ca37a3)

![image](https://github.com/Mohammed-Salameh/Network-emulators/assets/140098574/27387358-8ba0-4700-8f5c-caa6f300721e)

## Troubleshooting

- **Connection Issues:** Ensure your EVE-NG server's IP address is correct and that it's accessible from your network. Verify that the SFTP port (22) is not blocked by your firewall.
- **Permission Errors:** If EVE-NG can't access the appliance, ensure you've set the permissions correctly to `755`.
- **Appliance Not Showing:** Double-check that you've uploaded the files to the correct directory and that the directory name matches the appliance name.

---

This guide aims to simplify the process of uploading appliances to your EVE-NG environment using FileZilla.
