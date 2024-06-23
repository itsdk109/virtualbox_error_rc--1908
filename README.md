# Error 👇
![VirtualBox Error](https://github.com/itsdk109/virtualbox_error_rc--1908/blob/main/error.png)

# Kernel driver not installed (rc=-1908)

The error message you're seeing indicates that the VirtualBox kernel modules are not loaded correctly on your Linux system. Here are the steps you can follow to resolve this issue:


1. ## **Install necessary packages**:
   Ensure you have the required packages installed. This typically includes kernel headers and development tools. On Debian-based systems (like Ubuntu), you can install them with:
   ```bash
   sudo apt update
   sudo apt install build-essential dkms linux-headers-$(uname -r)
   ```

   ### On Red Hat-based systems (like Fedora), you can install them with:
   ```bash
   sudo dnf install @development-tools kernel-devel kernel-headers
   ```
   
2. ## **Run `vboxconfig` as root**:
   This command sets up the VirtualBox kernel modules.
   ```bash
   sudo /sbin/vboxconfig
   ```

3. ## **Restart your system**:
   After performing the above steps, restart your system to ensure that the changes take effect.

By following these steps, you should be able to resolve the error and get VirtualBox working on your Linux system.
