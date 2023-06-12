# homelab
An overview of my homelab personal project and all the services that I have on my home server!

## Table of Contents
- [Setting-Up Homelab](#setting-up-homelab)
    - [Pre-Requisites](#pre-requisites)
    - [Installing Proxmox Virtual Environment (VE)](#installing-proxmox-virtual-environment-ve)

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
6. To upload ISO Images navigate to local(proxmox) > ISO Images > upload and install VM's
    - Debian/Ubuntu systems install `apt-get install -y qemu-guest-agent`
    - Redhat based systems install `yum install -y qemu-guest-agent`

    Depending on the distribution, the guest agent might not start automatically after the installation.

    Start it either directly with

    `systemctl start qemu-guest-agent`

    Then enable the service to autostart (permanently) if not auto started with

    `systemctl enable qemu-guest-agent`

