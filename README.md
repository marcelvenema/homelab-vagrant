# GrIT Portable DevOps Training Omgeving
De GrIT Portable DevOps Training Omgeving is een compacte, portable omgeving welke geautomatiseerd een aantal virtuele machines installeert en configureert voor ontwikkel-, trainings- en demo doeleinden. De omgeving bestaat uit de volgende configuratie:

1. Lab: 3 virtuele machines, bestaande uit 1 master-node en twee worker-nodes.  Elk 2CPU, 2GB RAM, RockyLinux9 als OS.

# Prerequisites
Ondersteunde werkstations:
- Linux
- MacOS
- Windows

Ondersteunde hypervisors:
- Oracle VirtualBox
- libvirt (QEMU/KVM)
- ...

# Prerequisites
Alvorens deze omgeving te kunnen gebruiken, dient op het werkstation volgende software geinstalleerd te zijn:

[vagrant](https://vagrantup.com)
[virtualbox](https://virtualbox.org)
[vagrant-libvirt](https://github.com/vagrant-libvirt/vagrant-libvirt) Linux/MacOS only

Vagrant plugins:
Linux/MacOS: sudo dnf install @virtualization vagrant vagrant-libvirt vagrant-sshfs vagrant-hosts vagrant-cachier
Windows: vagrant plugin install vagrant-sshfs vagrant-hosts vagrant-cachier


# Start omgeving

```bash
vagrant up
```
Login in met gebruikersnaam vagrant, wachtwoord vagrant.

# Verwijder omgeving

```bash
vagrant destroy
```

# Beheer omgeving

vagrant suspend 
vagrant resume

# Run ansible provisioning from control-node

```bash
vagrant ssh master -c  "ansible-playbook /vagrant/provisioning/ansible/playbook.yml"
```