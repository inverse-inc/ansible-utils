# Ansible psonoci role

Install [psonoci](https://doc.psono.com/user/psonoci/install.html) binary from GitLab

## Requirements

N/A

## Variables

See [defaults variables](defaults/main.yml)

## Examples

```
- name: install psonoci
  hosts: all
  collections:
  - inverse_inc.utils
  
  roles:
  - psonoci
```
