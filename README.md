# Portable DevOps Training Lab

The Portable DevOps Training Lab environment (PDTL) is a compact, portable DevOps lab environment which automatically installs a number of virtual machines with HashiCorp Vagrant.


envorinment envoroOmgeving is een compacte, portable omgeving welke geautomatiseerd een aantal virtuele machines installeert en configureert voor ontwikkel-, trainings- en demo doeleinden. De omgeving bestaat uit de volgende configuratie:

1. Lab: 3 virtuele machines, bestaande uit 1 master-node en twee worker-nodes.  Elk 2CPU, 2GB RAM, RockyLinux9 als OS.

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


## Start environment

```bash
vagrant up
```
Login with username vagrant, password vagrant.

## Destroy environment

```bash
vagrant destroy
```

## Administration

vagrant suspend -
vagrant resume -

## Run ansible provisioning from control-node

```bash
vagrant ssh master -c  "ansible-playbook /vagrant/provisioning/ansible/playbook.yml"
```
