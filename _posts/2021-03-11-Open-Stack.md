---
published: true
layout: post
categories:
  - SDN
---
OpenStack adalah open source sistem operasi cloud yang mengontrol sumber daya computing, storage, dan network dalam jumlah besar. Semuanya dimanajemen dan disediakan melalui API dengan authentication yang umum.

![map openstack.PNG]({{site.baseurl}}/images/map openstack.PNG)


## Komponen
- **Nova**, Untuk fungsi computing
- **Neutron**, Untuk fungsi networking
- **Swift**, Untuk fungsi storage
- **Glance**, Untuk fungsi image os
- **Cinder**, Untuk fungsi block storage
- **Keystone**, Untuk fungsi identity 
- **Horizon**, Untuk fungsi dashboard

## Install

- Ubuntu 18.04
- RAM 2GB
- PROC 2 CORE

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-add-repository universe
sudo apt-get update
```
Tambahkan user stack
```
sudo adduser stack
sudo -i
echo "stack ALL=(ALL) NOPASSWD:ALL">>/etc/sudoers
exit
exit

==Login user stack==
git clone https://git.openstack.org/openstack-dev/devstack

chown -R stack devstack
cd devstack
sudo cp samples/local.conf ./local.conf
sudo nano local.conf
```

File local.conf
```
[[local|localrc]]
ADMIN_PASSWORD=secret
DATABASE_PASSWORD=$ADMIN_PASSWORD
RABBIT_PASSWORD=$ADMIN_PASSWORD
SERVICE_PASSWORD=$ADMIN_PASSWORD

HOST_IP=ipServerKita
```

Run
```
./stack.sh
```

### Source
---
1. [OpenStack Docs](https://docs.openstack.org/devstack/latest/)
2. [OpenStack](https://www.openstack.org/)
