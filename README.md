# Ceph-open-terrarium
<img src=".doc/pictures/terrarium.jpg" width=250px height=250px>

Ceph-open-terrarium lets deploy a ceph cluster on libvirt-kvm via terraform with saltstack or ansible or any other config mgmt tool.

# Install:

You need to install terraform  https://www.terraform.io/ and https://github.com/dmacvicar/terraform-provider-libvirt.

For the config management you will need to have saltstack or ansible installed on the machine executing the states/playbook.

# Examples:

Have a look at `examples` dir for how to use `ceph-open-terrarium`.

# Design-Architecture:

The architecture of project doesn't mix deployment with config management.
So you will be able to do `terraform apply` for preparing your KVM instances and use the config management of your choice for setup `ceph`

For explanation, remarks about the current Architecture design, have a look here [architecture](ARCHITECTURE.md)

### Deploy:

For saltstack and ansible you can use the ssh-key in dir `ssh_key`. This is passed by cloudinit.

Deployment will focus on libvirt-kvm.
ceph-open-terrarium will use https://github.com/dmacvicar/terraform-provider-libvirt  for deploying via terraform and cloudinit.

( Due to the modular nature of terraform, we might add terraform for cloud or other providers but for the first releases is out of scope.)

### Config Management:

In roadmap i plan to give support for saltstack and ansible

Ceph related
1) https://github.com/ceph/ceph-ansible
2) https://github.com/SUSE/DeepSea

# Roadmap:

Have a look on the roadmap board under github Projects.

# Contributing:

Take a look on [contributing](CONTRIBUTING.md)

# Authors:

- [Dario Maiocchi](https://github.com/MalloZup)

See also the list of [contributors](https://github.com/MalloZup/ceph-open-terrarium/graphs/contributors) who participated in this project.

