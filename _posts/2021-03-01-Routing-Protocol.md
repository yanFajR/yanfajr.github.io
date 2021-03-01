---
published: false
---
**Routing Protocol** adalah mekanisme atau aturan bagaimana paket-paket dikirimkan melalui jalur terbaik ke network tujuan.

## Jenis Routing Protocol

### Static

Static adalah bagaimana kita memberi tahu router jalur yang akan dilewati suatu paket dengan network tujuan tertentu secara manual.

Static routing akan sangat membantu ketika kita punya topologi network yang kecil, namun akan sangat merepotkan ketika kita memiliki topologi network yang besar.

Bandwith usage kecil, pengelolaan trafik mudah, dan keamanan lebih baik.

### Dynamic

Dynamic adalah ketika router bisa memahami jalur tujuan secara automatis dengan cara berbagi informasi mengenai alamat network antar router. 

## Jenis Protocol Routing Dynamic Secara Tempat Bekerjanya

### IGP

Interior Gateway Protocol merupakan routing protocol dinamis yang diterapkan untuk didalam suatu AS (Autonomus System). AS semacam instansi yang mengelola jaringannya sendiri. 

Contoh : RIP, OSPF, EIGRP, IGRP, IS-IS

### EGP

Exterior Gateway Protocol merupakan routing protocol yang digunakan untuk menghubungkan antar AS.

Contoh : BGP

## Jenis Protocol Routing Dynamic secara Algoritma

### Distance Vector

- Berfokus pada arah dan jarak dalam penentuan jalur terbaik.

- Tidak mengetahui topologi jaringan 

- Contoh : RIP, IGRP, EIGRP, BGP

- DV cocok untuk topologi jaringan sederhana

#### Kekurangan DV

- Routing Loops. misalnya pada suatu router(A) memiliki koneksi langsung ke suatu network(X), tetapi karena suatu insiden koneksi tersebut putus, lalu router sebelahnya(B) mengirimkan info ke A bahwa untuk menuju X bisa melalui B karena sebelumnya B belajar dari A mengenai tujuan ke X, Akhirnya terjadi loop paket dikirimkan bolak-balek antara A dan B hingga TTL habis. 

- Untuk mengatasi roting loop terdapat beberapa mekanisme diantaranya :
  - Split Horizon, Suatu router tidak memberi info rute suatu network kembali ke interface ia mempelajari network tersebut.
  - Hold-down timer, Mencegah suatu router memperbaharui info rute mengenai network yang terputus darinya dalam beberapa waktu.
  - Poison-reverse, Memperbarui ke router lain info rute yang terputus dengan nilai infinity yang artinya tidak mungkin dicapai melalui dirinya setelah menerima info rute dari router lain.
  - Triggered Update, Langsung memperbaharui info rute terputus dengan nilai infinity tanpa menunggu jadwal update.

### Link State

- Berfokus pada cost tersedikit dalam penentuan jalur terbaik.

- Mengetahui informasi topologi jaringan.

- Ada mekanisme untuk membangun hubungan dengan router tetangga.

- Butuh resource Memori dan CPU yang lebih karena paket-paket dan mekanisme protocolnya lebih banyak.

- Butuh BW yang sedikit, namun pada awal-awal butuh BW yang besar untuk menyusun topologi dan rute.

- Waktu convergance lebih cepat, ketika ada perubahan akan lebih cepat normal kembali.

- Contoh : OSPF, IS-IS

- Cocok untuk topologi jaringan berhirarki(core, distribution, access) 

## Routing Protocol Metrics
Untuk menentukan jalur terbaik yang akan dipilih dari sekian jalur yang ada.




