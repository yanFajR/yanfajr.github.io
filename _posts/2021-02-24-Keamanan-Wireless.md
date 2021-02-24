---
published: false
layout: post
categories:
  - Wireless
---
Wireless Network memilik kelemahan dalam keamanan dibandingkan dengan wired network, karena siapapun dapat dengan mudah terhubung ke suatu wireless network asalkan memiliki adapter wireless pada perangkatnya, oleh karena itu dibuatlah berbagai macam teknik untuk mengamankan wireless network.

### Hide SSID
![hidessid.PNG]({{site.baseurl}}/images/hidessid.PNG)
Untuk mengaktifkan keamanan hide SSID harus mendisable broadcast SSID, dan mengganti nama SSID default menjadi nama yang lain.

### WEP
![wep.PNG]({{site.baseurl}}/images/wep.PNG)
WEP adalah keamanan wireless yang sudah lama dan sekarang mudah untuk dicrack, sangat tidak dianjurkan untuk dipakai. Terdapat dua macam key yaitu yang panjangnya 10 dan 23 hex digit.

### WPA
![wpa.PNG]({{site.baseurl}}/images/wpa.PNG)
WPA adalah kemanan wireless yang lebih baru dibanding WEP. Terdapat 2 enkripsi yaitu AES dan TKIP, AES lebih baik dibanding TKIP, karena TKIP seperti WEP. WPA masih mudah untuk dicrack.

### WPA2
WPA2 adalah upgrade dari WPA sehingga lebih aman. Terdapat 2 enkripsi yaitu AES dan TKIP.

### MAC Filterring
![mf.PNG]({{site.baseurl}}/images/mf.PNG)
MAC Filterring bekerja dengan mendaftarkan alamat mac client yang dapat terhubung ke wireless network. Daftar tersebut akan dilakukan action diizinkan untuk join ke network atau ditolak.

