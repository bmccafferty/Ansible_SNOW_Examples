# Demo Script for Accelerators Demo

``` bash
# Login to podman Red Hat Registry
podman login registry.redhat.io

# Ensure in correct dir for demo
cd /root/git

# Since using Vault to encrypt SNOW PDI Login Details add vault
export ANSIBLE_VAULT_PASSWORD_FILE=.vault_password

# Run first Demo (Create INC) via ansible-navigator
ansible-navigator --mode stdout run  ~/git/Ansible_SNOW_Examples/playbooks/new_inc.yml -i ~/git/inventory/inv_files/lab.yml -l vm.bdm.scot


```