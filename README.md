# network-ansible
Ansible playbooks for managing network devices

**WARNING** These playbooks may perform destructive changes on your devices.  Do not use in production without proper testing.

## Usage:

 * Requires ansible 2.1 for `ios_command` and `ios_config`
 * Copy `devices.sample` to `devices` and update
 * Copy `./group_vars/all.sample` to `./group_vars/all` and update
```
cli:
  host: "{{ inventory_hostname }}"
  username: cisco
  password: cisco
  authorize: true
  auth_pass: cisco
```
 * Run Ansible with the selected playbook
```
ansible-playbook iosxe_upgrade.yml
```
