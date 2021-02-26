---
published: true
layout: post
categories:
  - Mikrotik
  - Network Management
---
Pada mikrotik bisa dilakukan konfigurasi radius karena mikrotik memiliki fitur radius sendiri. Radius sangat penting untuk manajemen Authentication, Authorization, dan Accounting.

**1. Cek Ip Mikrotik**
![ipaddr.PNG]({{site.baseurl}}/images/ipaddr.PNG)
disini saya akan menggunakan ip 192.168.0.106

**2. Setting pada User Manager**
- Masuk ke browser dengan alamat ipMikrotik/userman

![haluserman.PNG]({{site.baseurl}}/images/haluserman.PNG)
Jika belum setting user dan password, masuk saja dengan user "admin" dan password dikosongkan saja.

- Setting router yang akan ditambahkan radius

![routers.PNG]({{site.baseurl}}/images/routers.PNG)
Ip address 127.0.0.1 karena mikrotik itu sendiri, untuk nama router dan secret terserah.

- Buat Limitasi, Profile, dan User

pada kuota satuanya Bytes, pada rate satuannya bits
![limit.PNG]({{site.baseurl}}/images/limit.PNG)

![profile.PNG]({{site.baseurl}}/images/profile.PNG)

![user.PNG]({{site.baseurl}}/images/user.PNG)


3. Setting pada Mikrotik menggunakan winbox
![radius.PNG]({{site.baseurl}}/images/radius.PNG)

setting pada hotspot server profile
![hotspotserverprofile.PNG]({{site.baseurl}}/images/hotspotserverprofile.PNG)

4. Testing
masukkan user dan password yang sudah dibuat
![budi.PNG]({{site.baseurl}}/images/budi.PNG)
