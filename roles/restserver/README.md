# Ansible restserver role

Configure HTTP API service daemon on Cumulus Linux.

## Requirements

N/A

## Variables

See [defaults variables](defaults/main.yml)

## Examples

```
- name: configure Cumulus Linux
  hosts: cumulus
  collections:
  - inverse_inc.cumulus
  
  roles:
  - restserver
```
