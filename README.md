# simple-k8s-cluster

This repository contains anisble roles and a playbook that will provision a basic Kubernetes cluster to the provided master and nodes in the [inventory.yaml](inventory.yaml) file.

## Pre-requisites

- CentOS7 has been installed on the master and nodes.
- Ensure the hostname of each machine is unique.
- [Setup SSH Keys](https://www.digitalocean.com/community/tutorials/how-to-configure-ssh-key-based-authentication-on-a-linux-server) on the master and nodes. The [inventory.yaml](inventory.yaml) file has been configured to look for SSH keys at `./ssh-keys`.
- Ensure each machine is able to reach the internet.

## Provisioning

The below steps are an example of how you can use this playbook to provision a Kubernetes cluster:

1. `cd` to the root directory of this repository.
2. Edit [inventory.yaml](inventory.yaml) to contain the details of the hosts you are provisioning to.
3. Execute `./provision.yaml`.