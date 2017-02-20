# Scipion on OpenStack

Ansible deployment of Scipion Web Tools (https://github.com/I2PC/scipion-web) cluster on OpenStack cloud.
Default number of worker nodes is 5, but it can be changed by setting variable **count**.

## Setup
1. Install ansible and shade.
2. Set Openstack client environment with OpenStack RC file.
3. Configure security groups, flavor name, key name and other variables in vars/* .

## Start Scipion Web Tools cluster

Scipion Web Tools cluster can be started in the following way:

```bash
ansible-playbook scipion.yml -e count=3 -e cluster_id=cl -e os=centos
```
where

* **count** is number of worker nodes
* **cluster_id** is cluster identification, it is used as suffix in instances and volume names
* **os** is preferred operating system, Two options (centos and ubuntu) are supported.
