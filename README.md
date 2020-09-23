[![](https://img.shields.io/travis/com/ckaserer/ansible-role-remote-desktop/master?style=flat-square)](https://travis-ci.com/ckaserer/ansible-role-remote-desktop)
![gplv3](https://img.shields.io/badge/license-GPL%20v3.0-brightgreen.svg?style=flat-square)
![Maintenance](https://img.shields.io/maintenance/yes/2020?style=flat-square)

# ckaserer.remote-desktop

---

Either way we need to install the latest version of the desktop ansible role from ansible galaxy via

```
ansible-galaxy install ckaserer.desktop
```

---

## Default

The playbook below installs a desktop environment on all hosts.
Alternativly you can set `hosts` to a group of ansible nodes or `localhost`.
Executing the role requires root privileges hence the additional `become: true` in the `include_role` task.

```
- hosts: all
  tasks:
    - name: "Include ckaserer.remote-desktop"
      include_role:
        name: "ckaserer.remote-desktop"
        apply:
          become: true
```

---
