# Automated Terminal Setup with Kitty, Oh My Zsh and Ansible

This repository contains an Ansible playbook for automated terminal setup using `kitty` and `zsh` with the `Oh My Zsh` framework and several useful plugins.

## Pre-requisites

Before running this playbook, make sure you have Ansible installed on your machine. To install Ansible, follow the [official instructions](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

## Repository Structure

The repository structure is:

.
├── inventory
├── playbooks
│ └── setup.yml
└── roles
├── kitty
│ ├── files
│ │ └── kitty.conf
│ └── tasks
│ └── main.yml
└── zsh
├── handlers
│ └── main.yml
├── tasks
│ └── main.yml
├── templates
│ └── .zshrc.j2
└── vars
  └── main.yml

## How to Use the Repository

1. Clone the repository on your local machine.
2. Make sure the `inventory` file is configured correctly with the target machines.
3. Review and customise the settings in the files inside the `roles` folder if necessary.
4. Run the playbook with the following command:

   ```sh ansible-playbook -i inventory playbooks/setup.yml```
   
## Customization

# Kitty

The `kitty` configuration file is located in `roles/kitty/files/kitty.conf`. You can modify this file to adjust `kitty`'s configuration to your preferences.

# Oh My Zsh


`Oh My Zsh` plugins and theme can be customised in `roles/zsh/vars/main.yml`. The `.zshrc` file template is in `roles/zsh/templates/.zshrc.j2`, which you can adjust as needed.
