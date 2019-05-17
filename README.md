 Ansible role for basic workstation packages
-----------------------------------------------
[![Build Status](https://travis-ci.org/chaos-bodensee/role_install_workstaton_packages.svg?branch=master)](https://travis-ci.org/chaos-bodensee/role_install_workstaton_packages)

Ansible Playbook to install some packages, you usually need on workstations and laptops for your basic use.

Have a look into the ``vars/main.yml`` File to find out which packages will be installed.

Have a look into ``defaults/main.yml`` if you want to change some default parameters. A few of them a described below:


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

