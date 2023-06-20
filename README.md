**Ansible Playbook**

This repository contains an Ansible playbook that automates the installation and configuration of Pi-hole and Unbound on Ubuntu systems.

**Playbook Structure**

The playbook contains the following tasks:

- Updating and upgrading system packages
- Installing necessary dependencies such as curl, dnsutils, and netcat
- Installing and configuring Unbound

**Usage**

To use this playbook, follow these steps:

1. Make sure Ansible is installed on your machine
2. Clone this repository using the command:
```shell
git clone https://github.com/yourusername/yourrepository.git
```
3. Navigate to the repository's directory with:
```shell
cd yourrepository
```
4. Run the playbook using:
```shell
ansible-playbook -i your_inventory_file install_pihole_and_unbound.yml -K
```
Replace `your_inventory_file` with the path to your Ansible inventory file.

**Calling Role in Playbook**

To call this role in your playbook, use the `include_role` task:
```shell
- include_role:
    name: yourrepository
```
Replace `yourrepository` with the name of this repository in your system.

**Requirements**

- Ansible 2.10 or later

**License**

This project is licensed under the [MIT License](LICENSE).

---

Remember to replace `yourusername` and `yourrepository` with your Github username and the name of your repository respectively, and `install_pihole_and_unbound.yml` with the actual name of your Ansible playbook file.
