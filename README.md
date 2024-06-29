# ansible
Repo for Ansible roles developed for NetApp Ansible modules and playbooks

# scb-ontap-deploy
 
# ONTAP Select Deployment with Ansible

This Ansible playbook automates the deployment of NetApp ONTAP Select on a VMware environment.

## Directory Structure

- `ansible.cfg`: Ansible configuration file.
- `inventory/hosts`: Inventory file containing VMware and ONTAP nodes.
- `group_vars/all.yml`: Group variables for VMware and ONTAP Select configuration.
- `main.yml`: Main playbook to execute the roles.
- `roles/prepare_vmware`: Role to prepare the VMware environment.
- `roles/na_ots_deploy`: Role to deploy and configure ONTAP Select Deploy.
- `roles/na_ots_cluster`: Role to deploy and configure ONTAP Select cluster

## Usage

1. Update the `inventory/hosts` file with your VMware and ONTAP node details.
2. Update the `group_vars/all.yml` file with your VMware and ONTAP configuration.
3. Run the playbook:

```bash
ansible-playbook main.yml


ansible-playbook ots_setup.yaml --extra-vars deploy_pwd=$'"P@ssw0rd"' --extra-vars vcenter_password=$'"P@ssw0rd"' --extra-vars ontap_pwd=$'"P@ssw0rd"' --extra-vars host_esx_password=$'"P@ssw0rd"' --extra-vars host_password=$'"P@ssw0rd"' --extra-vars deploy_password=$'"P@ssw0rd"'