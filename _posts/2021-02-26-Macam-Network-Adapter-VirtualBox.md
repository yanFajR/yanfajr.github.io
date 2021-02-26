---
published: false
layout: post
categories:
  - Virtualisasi
---
VirtualBox merupakan hypervisor type dua yang menjalankan guest os diatas host os.
![]({{site.baseurl}}/images/Vb.PNG)


Network adapter pada VirtualBox :
**- Not attached**

Artinya tidak menyertakan network adapter

**- NAT**

Membuat network baru hasil nat host os
![Nat.PNG]({{site.baseurl}}/images/Nat.PNG)

**- NAT Network**

Sama seperti NAT hanya saja jika ada dua atau lebih guest yang terhubung menggunakan NAT Network berada dalam segmen network NAT yang sama.

**- Bridged Adapter**

Bridged membuat guest os seperti berada di segemen network yang sama seperti host os
![Bridge.PNG]({{site.baseurl}}/images/Bridge.PNG)

Kita bisa memilih adapter host mana yang akan dibridge

**- Internal Network**

Membantu untuk menghubungkan antar guest secara langsung
![intnet.PNG]({{site.baseurl}}/images/intnet.PNG)

Name harus sama antar kedua guest
![syaratnet.PNG]({{site.baseurl}}/images/syaratnet.PNG)

**- Host-only Adapter**

Seperti guest os membentu segemen network sendiri dan tidak terhubung ke host os
![adapter-only.PNG]({{site.baseurl}}/images/adapter-only.PNG)



