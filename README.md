# homelab
An overview of my homelab personal project and all the services that I have on my home server!


## Pre-Requisites
From a fresh install, the host computer requires

- `vim` install via `sudo apt install -y vim`
- `git` with ubuntu install via `sudo apt install -y git`
- `pip` install via `sudo apt install -y python3-pip`
- `ansible` install via `sudo python3 -m pip install -y ansible`
    - Add `PATH=$PATH:$HOME/.local/bin` to `~/.bashrc` and `source`
    - Add linting for syntax highlighting via `sudo pip install ansible-lint`
    - Create `/etc/ansible/hosts` file and directory and populate with target installs
