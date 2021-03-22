---
published: true
layout: post
categories:
  - Network Design
---
Perancangan jaringan hendaklah mengikuti metode yang benar agar jaringan yang akan dibuat memiliki nilai yang lebih. Merancang jaringan bukan hanya seperti connect the dot. Metode perancangan jaringan yang baik adalah Top-Down, artinya perancangan jaringan dimulai dari aspek layer 7 hingga layer 1 (application, presntation, session, transport, network, data link, physical).

Adapun tahapan perancangan jaringan (PDIOO)
- Plan

Identifikasi kebutuhan jaringan
- Design

Mendesain topologi secara logical dan physical
- Implement

Implementasi desain jaringan
- Operate

Menggunakan jaringan yang telah dirancang dengan tetap melakukan monitoring kualitas
- Optimize

Peningkatan performa dan perbaikan terhadap masalah jaringan

## Analisis tujuan bisnis dan kekangan
Sangat perlu mengetahui tujuan bisnis yang ingin dicapai melalui rancangan jaringan yang akan dibuat, agar rancagan tidak hanya dianggap bagus tetapi juga memenuhi keinginan yang hendak dicapai. Segala kekangan masalah yang dapat mempengaruhi rancangan jaringan perlu sejak dini diidentifikasi agar tidak menghabat proses perancangan, seperti budget, waktu, dan lain-lain.

## Analaisis tujuan teknis dan tradeoffs
Tujuan teknis
- **scalability**, mengenai kemampuan rancangan untuk memenuhi perkembangan kebutuhan jaringan.
- **availability**, mengenai kemampuan rancangan untuk menyediakan jaringan yang selalu aktif 100%.
- **network performance**, mengenai statistik througput, error rates, akurasi, efisiensi, waktu respon, delay, dll yang bagus.
- **security**, mengenai rancangan yang mampu memberikan pengamanan terhadap asset dan resource yang ada.
- **manageability**, mengenai kemampuan untuk memanajemen fault, configuration, accounting, performance, dan security.
- **usabilty**, mengenai kemudahan pengaksesan resource jaringan.
- **adaptability**, mengenai kemampuan rancangan yang dapat mengadaptasi teknologi terbaru dimasa mendatang.
- **affordability**, mengenai biaya yang dikeluarkan harus memenuhi kebutuhan.

## Karakterisasi Existing Jaringan dan Trafik
Tujuannya untuk mengidentifikasi kebutuhan dan menyesuaikan atara ekspektasi dan kondisi.

## Desain Topologi Jaringan
### Hirarki desain
- Core
  - Penghubung ke perangkat end.
- Distribution
  - Penghubung core dan access
- Access
  - Penghubung ke internet
  
### Redundant desain
- Backup path
  - satu mati satu ganti
- Load sharing
  - berbagi beban 
  
### Modular desain
Dipisah menjadi modul-modul dengan fungsi tersendiri

### Secure desain
- Policy keamanan
- Firewall

## Routing & Switching

Multiple Routing Protocol in an Internetwork
- CORE
  - ada redundant link, load sharing antar equal cost path.
  - eigrp, ospf, is-is.
  - ada mekanisme perubahan link dengan cepat jika terjadi fail pada suatu link.
- AKSES
  - RIPV2, OSPF, EIGRP
  
## Rancangan Keamanan Jaringan

### Perancangan keamanan jaringan:
1. identifikasi aset jaringan
2. analisis resiko keamanan
3. analisis kebutuhan dan tradeoff keamanan
4. pengembangan rencana keamanan
5. menentukan kebijakan keamanan
6. pengembangan prosedur untuk menerapkan kebijakan keamanan
7. pengembangan strategi teknsi implementasi
8. mendapatkan dukungan dari pengguna, manajer, dan staf teknis
9. pelatihan pengguna, manejer, dan staf teknis
10. implementasi prosedur keamanan dan strategi teknis
11. pengujian keamanan dan pembaruan jika ada masalh yang ditemukan.

### Resiko keamanan jaringan
- kehilangan informasi
- kerusakan informasi

resiko = ancaman x kelemahan

### Security tradeoffs
- affordability
- usability
- performance
- avaiability
- manageability

### kebijakan keamanan -> prosedur keamanan

### Mekanisme keamanan
- keamanan fisik
- AAA
- ENKRIPSI
- paket filter
- firewall
- IDS

### Rancangan keamanan secara modular
- defence in depth
- belt and suspenders, harus memiliki backup



## Strategi Manajemen Jaringan

- Rancangan manajemen jaringan yang baik dapat mencapai tujuan ketersediaan, performa, dan keamanan.

### Network Management Design
- Pertimbangan skalabilitas, trafic patterns, data formats, cost/benefit tradeoffs
- Tentukan sumberdaya yang akan dipantau
- Matrik pengukuran performa
  - availability
  - response time
  - throughput
  - usability
- Tentukan apa dan seberapa banyak data akan dikumpulkan

### Proaktive Network Management
- Pemeriksaan kesehatan jaringan selama operasi normal
  - potensi permasalahan
  - mengoptimalkan unjuk kerja
  - merencanakan pembaruan

### Network management process
- Fault Management
  - Mendeteksi, mengisolasi, mendiagnosa, memperbaiki masalah
  - melaporkan status keapada end user dan manager
  - melacak trend permasalahan
  - pengembangan solusi terhadap permasalahan

- Configuration Management
  - pelacakan terhadap piranti dan konfigurasinya
  - mengelola inventaris aset-aset jaringan
  - version-loging, melacak versi sistem operasi jaringan
  - manajer jaringan dapat menentukan dan menyimpan konfigurasi 

- Accounting Management
  - melacak menggunaan resource jaringan
  - menfasilitasi penggunaan billing
  - mencari penggunaan-penggunaan tidak wajar

- Performance jaringan
  - mengukur perilaku dan efektifitas jaringan

- Security Management
  - mengelola dan mendistribusikan user name dan passowrd
  - membangkitkan, mendistribusikan, dan meyimpan encription keys
  - meliputi tool dan reports untuk menganalisisi konfigurasi piranti untuk ketundukan terhadap standar keamanan

### Arsitektur network management
- Komponen 
  - a manage device 
  - an agent
  - a network management system
- Jalur
  - inband vs out of band
- Pemantauan
  - terpusan vs terdistribusi

### SNMP
- SNMPV3 menawarkan autentikasi
- MIB (Management Information Base)

### RMON
- mengatasi kelemahan penyediaan statistic parameter pada lapisan data link dan physic.

### Cisco Tools 
- CDP (Cisco Discovery Protocol)
  - menentukan bagaimanan perangkat cisco bertukar info konfigurasi
- Cisco NetFlow Accounting
  - mengumpulkan dan mengukur data yang masuk ke interface router autau switch

### Estimasi Trafik Network Management
- Misal ada 200 piranti, 10 parameter tiap piranti
  request = 2000
- Setiap paket 64 byte/5 detik
  2000*2*64 bytes/5 detik
- Bandingkan dengan bandwith, apakah wajar atau tidak
