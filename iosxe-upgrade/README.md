Upgrades rommon and system image for ASRs running IOS XE

Usage:

 * Requires ansible 2.1 for `ios_command` and `ios_config`
 * Update inventory to include your device(s) hostname/ip
 * Update upgrade.yml with username/password
```
    cli:
      host: "{{ inventory_hostname }}"
      username: cisco
      password: cisco
```
 * Run Ansible - device will reboot TWICE!
```
ansible-playbook -i inventory upgrade.yml
```
