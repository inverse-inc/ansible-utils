# Ansible mailhog role

Installs [MailHog](https://github.com/mailhog/MailHog), a Go-based SMTP server and web UI/API for displaying captured emails, on RedHat or Debian-based linux systems.

Also installs [mhsendmail](https://github.com/mailhog/mhsendmail) so you can redirect system mail to MailHog's built-in SMTP server.

## Requirements

N/A

## Variables

See [defaults variables](defaults/main.yml)

`mailhog__env_vars` is specific and can be used to configure MailHog using
[environment
variables](https://github.com/mailhog/MailHog/blob/master/docs/CONFIG.md). Environment
variables are set in a dedicated environment file, sourced by systemd unit
used to start MailHog. In any cases, they are defined for all processes.

Example:

```yaml
mailhog__env_vars:

  # Listen on port different than 1025 to avoid conflict with HAProxy
  - name: "MH_SMTP_BIND_ADDR"
    value: "127.0.0.1:2525"

  - name: "MH_API_BIND_ADDR"
    value: "127.0.0.1:8025"

  - name: "MH_UI_BIND_ADDR"
    value: "127.0.0.1:8025"
``` 

## Examples

```
- name: install mailhog
  hosts: all
  collections:
  - inverse_inc.utils
  
  roles:
  - mailhog
```

## Author Information

This role was created in 2014 by [Jeff
Geerling](https://www.jeffgeerling.com/), author of [Ansible for
DevOps](https://www.ansiblefordevops.com/) and forked in 2020 by Inverse inc.
