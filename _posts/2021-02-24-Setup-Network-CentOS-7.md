---
published: true
layout: post
categories:
  - Linux
---
Mengatur network centos7 saat pertama kali diinstall

**1. Cek network interface yang digunakan**
>nmcli d

![nmcli d]({{ site.baseurl }}/images/nmclid.PNG)

**2. Edit file konfigurasi network sesuai dengan interface yang digunakan**
>vi /etc/sysconfig/network-scripts/ifcfg-ens33

![netconf]({{ site.baseurl }}/images/netconf.PNG)

**3. Restart service network**
>systemctl restart network

**4. Test koneksi**
>ping google.com
