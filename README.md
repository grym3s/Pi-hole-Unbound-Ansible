# Pi-hole with Unbound

This repository contains an Ansible playbook for setting up and configuring a Pi-hole with Unbound on specified hosts. Unbound is a local DNS server providing DNSSEC validation. This playbook changes the upstream DNS server in Pi-hole to `127.0.0.1#5335`.

## Playbook Details

The playbook consists of a single `main.yml` file which performs the entire setup and configuration.

## Usage

Follow these steps to use this playbook:

1. Ensure you have Ansible installed on your local machine.
2. Clone this repository:

```bash
git clone https://github.com/grym3s/Pi-hole-Unbound-Ansible.git
```

3. Navigate into the repository directory:

```bash
cd pihole-unbound
```

4. Update the `hosts` file with your target hosts.
5. Run the playbook using the following command:

```bash
ansible-playbook main.yml -i hosts
```

Make sure to replace `hosts` with your actual hosts file.

## Requirements

- Ansible 2.10 or later

## License

This project is licensed under the [MIT License](LICENSE).
