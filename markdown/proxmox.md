# Installing Proxmox Virtual Environment (VE)

[Click Here](../README.md) to go back to the **README.md**

---

From applications list open Virtual Machine Manager and follow the following steps:

1. From file choose Create VM
2. Use Proxmox `.iso` image
   - Choose `Debian 10`
3. Decide the resources allowed for Proxmox, I used
   - 10Gb of RAM of my available 16Gb
   - 6 of my 8 allowable Cores
   - 256Gb of storage of available 1Tb
4. Choose the FDQN name to be `proxmox.local`
5. After reboot on host computer navigate to the listed browser url and login with user `root` using the password you created
   - At this point the VM can be converted to a template, step 6 to be repeated for _each_ VM
6. To upload ISO Images navigate to local(proxmox) > ISO Images > upload and install VM's

   - Debian/Ubuntu systems install `sudo apt-get install -y qemu-guest-agent`
   - Redhat based systems install `yum install -y qemu-guest-agent`

   Depending on the distribution, the guest agent might not start automatically after the installation.

   Start it either directly with

   `systemctl start qemu-guest-agent`

   Then enable the service to autostart (permanently) if not auto started with

   `systemctl enable qemu-guest-agent`

   With this completed, restart/reboot the VM and under proxmox summary, you should see the VM's IP address listed and available for remote SSH

---

[Click Here](../README.md) to go back to the **README.md**
