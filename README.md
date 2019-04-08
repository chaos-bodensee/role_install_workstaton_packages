 Ansible role for basic workstation packages
-----------------------------------------------
[![Build Status](https://travis-ci.org/DO1JLR/role_install_workstaton_packages.svg?branch=master)](https://travis-ci.org/DO1JLR/role_install_workstaton_packages)

Ansible Playbook to install basic packages *(needed for workstaion)*.

Have a look into the default variables to expand what should be installed in your config.

You can change the packages by defining this variables yourself.

If you think here is missing something... Pleas create a pull-request or at least a issue.

### config:
If you won't have cups enabled and installed set the following variable:
```
install_cups: false #(default is true)
```

