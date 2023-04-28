# Portable DevOps Training Lab

The Portable DevOps Training Lab (PDTL) is a compact, portable DevOps lab environment which automatically installs a number of virtual machines with HashiCorp Vagrant.

1. Lab: 3 virtuele machines, one master-node and two worker-nodes.  Each 2CPU, 2GB RAM, RockyLinux9 operating system.

## Prerequisites

Supported platforms:

- Linux
- MacOS
- Windows

Supported hypervisors:

- Oracle VirtualBox
- libvirt (QEMU/KVM)
- ...

Before using the environment, please be sure you have installed the following software:

[vagrant](https://vagrantup.com)
[virtualbox](https://virtualbox.org)
[vagrant-libvirt](https://github.com/vagrant-libvirt/vagrant-libvirt) Linux/MacOS only

Vagrant plugins:
Linux/MacOS: sudo dnf install @virtualization vagrant vagrant-libvirt vagrant-sshfs vagrant-hosts vagrant-cachier
Windows: vagrant plugin install vagrant-sshfs vagrant-hosts vagrant-cachier

## Getting Started

Clone this repository to a folder on your host with command:

```cmd
git clone https://github.com/marcelvenema/homelab-vagrant.git
```

Go to the folder and type:

```cmd
vagrant up
```

Login with username vagrant, password vagrant.

## Destroy environment

```cmd
vagrant destroy
```

## Administration

vagrant suspend -
vagrant resume -

## Run ansible provisioning from control-node

```cmd
vagrant ssh master -c  "ansible-playbook /vagrant/provisioning/ansible/playbook.yml"
```
