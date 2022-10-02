# Demo Script for Accelerators Demo

``` bash
# Env used, RHEL 8.5 AAP 2.2, servicenow.itsm 2.0.0

# Login to podman Red Hat Registry
podman login registry.redhat.io

# Ensure in correct dir for demo
cd /root/git

# Since using Vault to encrypt SNOW PDI Login Details add vault
export ANSIBLE_VAULT_PASSWORD_FILE=.vault_password

# Run first Demo (Create INC) via ansible-navigator
ansible-navigator --mode stdout run  ~/git/Ansible_SNOW_Examples/playbooks/new_inc.yml -i ~/git/inventory/inv_files/lab.yml -l vm.bdm.scot

# Show Next Demo on Controller (INC Survey)

# Run 2nd Demo (Create CHG) via ansible-navigator
ansible-navigator --mode stdout run  ~/git/Ansible_SNOW_Examples/playbooks/new_chg.yml -i ~/git/inventory/inv_files/lab.yml -l vm.bdm.scot

# Show Next Demo on Controller (CHG Survey)

# Bring it all together and show patching play with checking chg state, moving state and error on fail

# Raise New Change for Patching Demo via Controller
# Show Change in SNOW and move to scheduled
# Start play on working host (rhel8)
# Show complete state in SNOW

# Raise New Change for Patching Demo via Controller
# Show Change in SNOW and move to scheduled
# Start play on broken host (rhel8-test)
# Show Failed Change & INC Number in SNOW

# Q&A

# [Slide Deck](https://docs.google.com/presentation/d/1BdHwvDWtBvc_DTvyPvHOZr6JTI5bZVMNLcssjjRq0xY/edit?usp=sharing) (Requires RH Account)


```