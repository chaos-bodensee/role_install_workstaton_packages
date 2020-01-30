 Ansible role for basic workstation packages
=========================================

[![Build Status](https://travis-ci.org/chaos-bodensee/role_install_workstaton_packages.svg?branch=master)](https://travis-ci.org/chaos-bodensee/role_install_workstaton_packages)

Ansible Playbook to install some basic packages and desctop packages, you could need to enjoy your linux desktop.

 Which packages
--------------
Have a look into the ``vars/main.yml`` File *[github](https://github.com/chaos-bodensee/role_install_workstaton_packages/blob/master/vars/main.yml))* to find out which packages will be installed.
Please be aware that not all packages are available at every linux distribution!

 default settings
----------
Have a look into ``defaults/main.yml`` *([github](https://github.com/chaos-bodensee/role_install_workstaton_packages/blob/master/defaults/main.yml))* you want to change some default parameters. A few of them a described below:


### config:
If you won't have cups enabled and installed set the following variable:
```bash
install_cups: false #(default is true)
```

If you don't want a version check:
```bash
submodules_versioncheck: false # (default is true)
```

If you wan't some additional packages on your OS:
```bash
install_extra_workstation_packages:
  - foo
  - bar
```

 Installation:
----------------

### Using ansible galaxy
```bash
# installation
ansible-galaxy install do1jlr.role_install_workstaton_packages
```

```yaml
---
# example playbook
- name: install some base and desktop packages
  roles:
  - do1jlr.role_install_workstaton_packages
```

# without ansible galaxy
```bash
# installation
git clone https://github.com/chaos-bodensee/role_install_workstaton_packages.git roles/workstation_packages
```

```yaml
---
# example playbook
- name: install some base and desktop packages
  tags:
   - packages
   - default
  roles:
    - workstation_packages
```

 Recomended additional ansible repos to install useful packages:
----------

| package name | github url | ansible galaxy |
| ------------ | ---------- | -------------- |
| ``ranger`` *(file manager)* | [github.com/chaos-bodensee/role-ranger](https://github.com/chaos-bodensee/role-ranger.git) | *(comming soon)* |
| ``bat`` | [https://github.com/gantsign/ansible_role_bat](https://github.com/gantsign/ansible_role_bat) | *(soon)* |


 Contribute
-----------
If something is not working properly, please feel free to open an issue! *(Or even better: Create a pull-request)* <br />
If you are missing something, please leave a issue *(or a pull-request)*!
