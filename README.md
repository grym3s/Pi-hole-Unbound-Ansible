
# Pi-hole with Unbound

This project contains an Ansible playbook used for setting up and configuring a Pi-hole with Unbound on specified hosts. Unbound is used as a local DNS server which provides DNSSEC validation. This playbook changes the upstream DNS server in Pi-hole to `127.0.0.1#5335`, pointing to the local Unbound instance.

## Structure

This playbook operates on the `pihole_hosts` group, performing tasks for installing Unbound and configuring Pi-hole.

### Main Playbook

The main playbook file is `main.yml`, which is executed against all hosts specified in the Ansible inventory.

### Task Files

Tasks are split into separate files for easier management:

- `install_unbound.yml`: This file includes tasks to install Unbound and set it up.

- `configure_pihole.yml`: This file includes tasks to change the upstream DNS server in Pi-hole to point to the local Unbound instance and restarts the FTL service to apply changes.

## Usage

To execute the playbook, follow these steps:

1. Ensure you have Ansible installed on your local machine.

2. Clone this repository:

   ```
   git clone https://github.com/your-github-username/pihole-unbound.git
   ```

3. Change into the repository directory:

   ```
   cd pihole-unbound
   ```

4. Update the inventory file (e.g., `inventory.ini`) with your target hosts and groups.

5. Run the playbook using the following command:

   ```
   ansible-playbook main.yml -i inventory.ini
   ```

   Make sure to replace `inventory.ini` with your actual inventory file.

## Support

For help and support, please submit an issue in the issue tracker.

## Contributing

We're open to any contributions. If you find a bug or have a feature request, please create an issue to discuss it. If you wish to contribute code, please fork the repository, create a new branch for your feature, and issue a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

## Project status

Active

Please replace the GitHub URL in step 2 with your actual GitHub repository URL. This README is an initial structure and may require further edits based on the specific needs and aspects of your project.
