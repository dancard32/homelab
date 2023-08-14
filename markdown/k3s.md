# Initializing a k3s Kubernetes Cluster

[Click Here](../README.md) to go back to the **README.md**

---

Initializing a kubernetes cluster can be difficult - but it doesn't have to be. With Ansible and a populated `inventory.ini` we can specify the host servers and agents and initialize a cluster with a quick ansible playbook.

This can be achieved with the following command

    ansible-playbook k3s_install.yml -i inventory.ini -K

Additionally,

> **Note:** If Installing to ARM/Raspberry Pi, add the following to `/boot/cmdline.txt`


    cgroup_memory=1 cgroup_enable=memory


Refer to [k3s-ansible/Issue on Rasbian x64 #179](https://github.com/k3s-io/k3s-ansible/issues/179)

Un-installing the kubernetes cluster can be achieved through the following

    ansible-playbook k3s_reset.yml -i inventory.ini -K

Future work is either to refactor and prompt the user for a high-available k3s cluster, or either have separated roles for whatever configuration that is desired

---

[Click Here](../README.md) to go back to the **README.md**
