# ansible
Repo for Ansible roles developed for NetApp Ansible modules and playbooks

# scb-ontap-deploy
 
# ONTAP Select Deployment with Ansible

This Ansible playbook automates the deployment of NetApp ONTAP Select on a VMware environment.

## Directory Structure

- `ansible.cfg`: Ansible configuration file.
- `inventory/hosts`: Inventory file containing VMware and ONTAP nodes.
- `group_vars/all.yml`: Group variables for VMware and ONTAP Select configuration.
- `playbook.yml`: Main playbook to execute the roles.
- `roles/prepare_vmware_environment`: Role to prepare the VMware environment.
- `roles/deploy_ontap_select`: Role to deploy and configure ONTAP Select.

## Usage

1. Update the `inventory/hosts` file with your VMware and ONTAP node details.
2. Update the `group_vars/all.yml` file with your VMware and ONTAP configuration.
3. Run the playbook:

```bash
ansible-playbook main.yml
