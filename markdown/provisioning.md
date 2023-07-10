# Provisioning
I have used Ansible to automate hardware provisioning to streamline deployment

- `vim` install via `sudo apt install -y vim`
- `git` with ubuntu install via `sudo apt install -y git`
- `pip` install via `sudo apt install -y python3-pip`
- `ansible` install via `sudo python3 -m pip install -y ansible`
    - Add `PATH=$PATH:$HOME/.local/bin` to `~/.bashrc` and `source`
    - Add linting for syntax highlighting via `sudo pip install ansible-lint`
    - Create `/etc/ansible/hosts` file and directory and populate with target installs

Hardware provisioning on the local hardware can be completed with the following ansible playbook

    ansible-playbook hw_provisioning.yml --limit=localhost -K

If you would like to provision all the specified machines found in the `ansible/inventory.ini` run the following

    ansible-playbook hw_provisioning.yml -i inventory.ini -K

---
[Click Here](../README.md) to go back to the **README.md**