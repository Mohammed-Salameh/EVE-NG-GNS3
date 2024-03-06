
# Troubleshooting Guide for UNetLab Execution Errors

If you encounter errors while executing `/opt/unetlab/wrappers/unl_wrapper -a fixpermissions` on UNetLab, follow this guide to troubleshoot and resolve the issues. The errors may look like one of the following:

- PHP Notice: file_get_contents(): read of 8192 bytes failed with errno=21 Is a directory in /opt/unetlab/html/includes/init.php on line 71
- PHP Warning: file_get_contents(/opt/unetlab/platform): failed to open stream: No such file or directory in /opt/unetlab/html/includes/init.php on line 71

## Prerequisites

- Ensure you have root access to the UNetLab server.

## Troubleshooting Steps

### Step 1: Verify and Edit File Contents

1. Open the file `/opt/unetlab/html/includes/init.php`.
2. Check if the 71st line is as follows:
   ```php
   $kvm_family = file_get_contents("/opt/unetlab/platform");
   ```
   If the line differs, edit it to match the above.

### Step 2: Identify CPU Family and Update Platform File

1. Run the command to identify your CPU family:
   ```bash
   dmesg | grep -i cpu | grep -i -e intel -e amd
   ```
2. Based on the output, follow the appropriate step:
   - If the output includes "Intel", execute:
     ```bash
     echo "intel" > /opt/unetlab/platform
     ```
   - If the output includes "AMD", execute:
     ```bash
     echo "amd" > /opt/unetlab/platform
     ```

After completing these steps, try running `/opt/unetlab/wrappers/unl_wrapper -a fixpermissions` again. This should resolve the errors you were experiencing.
```

This markdown guide provides a structured approach to troubleshoot and fix the specified errors in UNetLab.
