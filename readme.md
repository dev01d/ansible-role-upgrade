# Ansible Ubuntu upgrade

Performs dist-upgrade, autoremove, and reboots the node if necessary.

```yaml
- hosts: '{{ host }}'
  become: yes
  vars:
    host: # Host group
  # Set facts for role digest
  # pre_tasks unnecessary if using default port 22
  pre_tasks:
    - name: Setting SSH facts
      set_fact:
        ssh_port: # non standard SSH port number
  roles:
    - upgrade
```
