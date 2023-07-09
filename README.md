# homelab
An overview of my homelab personal project and all the services that I have on my home server!

![Homelab Cover](images/homelab-cover.PNG)

## Table of Contents
- [Setting-Up Homelab](#setting-up-homelab)
    - [Pre-Requisites](#pre-requisites)
    - [Installing Proxmox Virtual Environment (VE)](#installing-proxmox-virtual-environment-ve)

- [References]()

---

## Setting-Up Homelab

### **Pre-Requisites**
From a fresh install, the host computer requires

- `vim` install via `sudo apt install -y vim`
- `git` with ubuntu install via `sudo apt install -y git`
- `pip` install via `sudo apt install -y python3-pip`
- `ansible` install via `sudo python3 -m pip install -y ansible`
    - Add `PATH=$PATH:$HOME/.local/bin` to `~/.bashrc` and `source`
    - Add linting for syntax highlighting via `sudo pip install ansible-lint`
    - Create `/etc/ansible/hosts` file and directory and populate with target installs

### **Installing Proxmox Virtual Environment (VE)**
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

## References
A big thank you for all the help from sites like Stack Overflow, Github, YouTube, and for people that offer help just like you!

Below is a list of all the references if you would like to know how I was able to build my homelab and its services:

- **Cloudflare Tunneling/Guacamole/Exposing Homelab**
    - [Meet Guacamole, Your Remote Access Gateway](https://www.youtube.com/watch?v=LWdxhZyHT_8)
    - [guacamole Remote Desktop Multiple Computers](https://www.youtube.com/results?search_query=guacamole+remote+desktop+multiple+computers)
- **General Homelab Services**
    - [What's On My Home Server? Storage, OS, Media, Provisioning, Automation](https://www.youtube.com/watch?v=f5jNJDaztqk&pp=ygULaG9tZWxhYiB2cG4%3D)
    - [Virtualize Ubuntu Server with Proxmox VE](https://www.youtube.com/watch?v=YR9SNDD8WB4)
    - [Proxmox VE Install and Setup Tutorial](https://www.youtube.com/watch?v=7OVaWaqO2aU&themeRefresh=1)
    - [My Proxmox Basic Initial Setup](https://www.youtube.com/watch?v=5axVd19Jris)
    - [How To Access Your PCs and Servers from Anywhere Using Guacamole and Cloudflare Tunnels](https://www.youtube.com/watch?v=tg1CbMEzCsc&pp=ygUUY2xvdWRmbGFyZSBndWFjYW1vbGU%3D)
    - [HomeLab Services Tour Late 2021 - What am I Self-Hosting in my HomeLab?](https://www.youtube.com/watch?v=IE5y2_S8S8U)
    - [EXPOSE your home network to the INTERNET!! (it's safe)](https://www.youtube.com/watch?v=ey4u7OUAF3c)
    - [access EVERYTHING from your web browser!! (Linux and Windows Desktop, SSH) // Guacamole Install ](https://www.youtube.com/watch?v=gsvS2M5knOw&pp=ygUgaG93IHRvIGluc3RhbGwgZ3VhY2Ftb2xlIGhvbWVsYWI%3D)
