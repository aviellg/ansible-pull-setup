#!/bin/bash # Update and upgrade the system apt-get update -y apt-get upgrade -y # Install Git and curl apt-get install -y git curl # Install Ansible apt-get install -y ansible # Execute ansible-pull with your configuration ansible-pull -U https://github.com/aviellg/ansible-pull-setup.git --force

# Ansible Pull Setup

This repository contains an Ansible setup to configure your local machine using `ansible-pull`.

## Prerequisites

1. Python 3.6 or higher
2. `pipx` for managing Python tools

## Installing Ansible using pipx

Follow these steps to install Ansible using `pipx`:

1. Update and upgrade your system package lists to ensure all applications are up-to-date.
2. Verify if `pipx` is installed. If it is not, proceed to install `pipx` using the package manager.
3. Use `pipx` to install Ansible, ensuring that all dependencies are included.
4. Inject `argcomplete` into Ansible to enable command completion features.
5. Confirm that the `pipx` binaries are included in your system's PATH.
6. Verify the installation by checking the installed version of Ansible.

## Running the Ansible Pull Setup

To use this repository with `ansible-pull`, execute the following:

- Use the `ansible-pull` command with the repository URL to pull the latest version of the playbook and execute it on your local machine.

## Repository Structure

- `tasks/`: Contains the main tasks to be executed.
- `handlers/`: Contains handlers to restart services when necessary.
- `templates/`: Contains templates for configuration files.
- `roles/`: Contains Ansible roles.
- `requirements.yml`: Lists the required roles for the setup.
- `local.yml`: The playbook to run with `ansible-pull`.

## Additional Resources

- This setup utilizes the Ansible role available at [ansible-role-setup](https://github.com/aviellg/ansible-role-setup).

## Contributing

Feel free to contribute by submitting a pull request or opening an issue. Contributions are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

