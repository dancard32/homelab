# Configuring Homelab

[Click Here](../README.md) to go back to the **README.md**

---

Although I have created my own homelab to suit my own needs and practices, every homelab has its own requirements to fill. The following are what will need to be user defined and tailored to their wants:

- Docker Services:

  Inside the `docker-compose.yml` the user will need to add/remove/update the services to what they would like. In addition specify the network because on a `docker compose up/down` the containers get re-assigned IP addresses which result in issues when connecting to CLoudflare.

  Note that if you would like to use Cloudflare then you must create an `.env` file at the top-level of this directory specifying your Cloudflare API key.

  Lastly, if persistent data is needed, add those directories to the `ansible/roles/docker_mkdir/tasks/main.yml` ansible role.

- Ansible:

  All that is required for Ansible is a populated inventory list that will be used while running ansible playbooks. An example can be found below

  > **Example:** Inventory.ini

      [proxmox]
      IP4_ADDRESS ansible_ssh_user=user ansible_ssh_pass=password

      [servers]
      IP4_ADDRESS ansible_ssh_user=user ansible_ssh_pass=password

      [nodes]
      IP4_ADDRESS ansible_ssh_user=user ansible_ssh_pass=password
      IP4_ADDRESS ansible_ssh_user=user ansible_ssh_pass=password
      IP4_ADDRESS ansible_ssh_user=user ansible_ssh_pass=password

      [k3s_cluster:children]
      servers
      nodes


- Kubernetes Services

  Installation of Kubernetes services will be managed through helm, configuring these services will be determined after they are fully functioning.

---

[Click Here](../README.md) to go back to the **README.md**
