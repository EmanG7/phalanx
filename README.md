phalanx
=========

Modular Proxmox Hardening Role

Requirements
------------



Role Variables
--------------

Modular variables to enable/disable parts of the hardening role are as follows in the table.

| Variables                    | How to use                                                     |
|------------------------------|----------------------------------------------------------------|
| `module_audit`               | Set to "false" to disable audit module. Defaults to "true".    |
| `module_firewall`            | Set to "false" to disable firewall module. Defaults to "true". |
| `module_fail2ban`            | Set to "false" to disable fail2ban module. Defaults to "true". |

Extra Variables

`disable_backup` -> Disables "Import config backup tasks" when set to "true". Default to "false".

Dependencies
------------



Security Features
-----------------



Example Playbook
----------------

Quick-Start Playbook
```yaml
- hosts: proxmox
  become: true
  roles:
    - phalanx
```
---
Modular Playbook
```yaml
- hosts: proxmox
  become: true
  roles:
    - role: phalanx
      module_audit: false
      module_firewall: true
      module_fail2ban: # undefined/blank -> defaults to true
      # ...
```

License
-------

BSD-3-Clause


