# Ansible Playbook to Deploy ZFS Storage

This repository contains Ansible Playbook to Deploy ZFS storage with various exporter for your Z Volumes like NFS and ISCSI.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.
See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Prequisites package:
* Python 3 (Python Programming Language)
* Python PIP (Python Package Installer & Manager)
* Ansible 2.6 (Simple IT Automation Tool)

### Deployment

Standard deployment:
* Install Python 3
* Install Python PIP
```
wget -q -O - https://bootstrap.pypa.io/get-pip.py | python3 -
pip3 install --no-cache-dir --upgrade pip setuptools wheel
```
* Install Ansible 2.6
```
pip3 install --no-cache-dir ansible==2.6.20
```
* Check Ansible and Ansible Playbook version
```
ansible --version
ansible-playbook --version
```
* Clone this repository to your current directory, make sure it's empty
```
git clone -b master https://github.com/dimaskiddo/ansible-zfs.git .
```

## Installing
* Modify inventory file
```
nano inventory/zfs
```
* Run playbook to configure ZFS storage
```
ansible-playbook -i inventory/zfs config.yml
```

## Uninstalling
* Run playbook to uninstall ZFS storage
```
ansible-playbook -i inventory/zfs uninstall.yml
```

Optional uninstall parameters:
* ```-e uninstall_nfs=true```, will also uninstall NFS server packages
* ```-e uninstall_iscsi-lio=true```, will also uninstall ISCSI LIO packages

## Built With

* [Python](https://www.python.org/) - Python Programming Language
* [Python PIP](https://pypi.org/project/pip/) - Python Package Installer & Manager
* [Ansible](https://www.ansible.com/) - Simple IT Automation Tool

## Authors

* **Dimas Restu Hidayanto** - *Initial Work* - [DimasKiddo](https://github.com/dimaskiddo)

See also the list of [contributors](https://github.com/dimaskiddo/ansible-zfs/contributors) who participated in this project
