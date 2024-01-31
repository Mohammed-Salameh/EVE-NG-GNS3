## Guide for Deploying Cisco Layer 2 Switch (vIOS-L2)

This guide provides step-by-step instructions on how to deploy a Cisco vIOS Layer 2 switch. Before starting, ensure you have the necessary vIOS-L2 IOS image for Cisco CCNA and Cisco CCNP exams.

### Prerequisites:
- vIOS-L2 IOS image file
- [QEMU](https://www.qemu.org/download/) installed on your system
- [GNS3](https://www.gns3.com/software/download) software for network device emulation

### Deployment Steps:

#### **Step 1: Configure QEMU Settings in GNS3**
1. Open GNS3.
2. Navigate to the menu bar and select `Edit` -> `Preferences`.
3. In the Preferences window, navigate to the `QEMU` section and then to `QEMU VMs`.

#### **Step 2: Create a New Virtual Machine**
1. Click the `New` button.
2. In the New VM setup:
   - **Name**: Enter `Cisco vIOS Layer 2 Switch`.
   - **Memory**: Set to `768 MB`.
   - **Binary**: Choose `qemu-system-x86_64`.
   - **Console Type**: Select `telnet`, `vnc`, or `spice` according to your preference.
3. Click `Next` to proceed.

#### **Step 3: Add the vIOS-L2 Image**
1. In the `New Image` section, click `Browse`.
2. Locate and select the `.vmdk` file for the vIOS-L2 IOS image.
3. Click `Open` to add the image.

#### **Step 4: Finalize Setup**
1. Review the settings and click `Finish` to complete the VM setup.

#### **Step 5: Deploy the Appliance**
1. In GNS3, drag and drop the newly created `Cisco vIOS Layer 2 Switch` to the workspace.
2. Connect it to your network topology as required.

### Important Notes:
- **Reboot Loop Issue**: If you encounter a reboot loop when starting the switch, increase the memory to `768 MB`.
- **Usage for Exams**: The vIOS-L2 IOS image is suitable for practicing Cisco CCNA and Cisco CCNP exam scenarios.

### Download Link:
For downloading the vIOS-L2 IOS image, use the following link: [Cisco vIOS-L2 Image](https://drive.google.com/file/d/1nsiaoTWi2345kUPgcs1-pLtDBjbBMHhM/view?usp=drive_link)

---

This guide is intended for educational purposes and to aid in network simulation for training. Make sure you comply with Cisco's software usage policies and only use software you're legally entitled to use.
