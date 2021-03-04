---
published: true
layout: post
categories:
  - Devnet
---
## Software Devlopment
Software development atau lebih dikenal dengan SDLC (software development life cycle) membicarakan bagaimana mengembangkan sebuah software dimulai dari mengidentifikasi kebutuhan, membuat proof konsep, testing, hingga memperbaik bug.

### Common Fase SDLC 
1. Analisis kebutuhan
   - Dimulai dari mengidentifikasi stakeholder, kebutuhan, hambatan, infrastruktur terkini dll.
   - Perlu diketahui tujuan apa yang hendak dicapai dengan software yang akan dibuat.
   - Sangat dianjurkan untuk membuat Dokumen Software Requirements and Scope (SRS).

2. Desain
   - Berdasarkan SRS
   - Akan dibuat dua document:
     - High Level Design (HLD)
       Menjelaskan arsitektur secara umum, komponen dan hubungan diantaranya, dan detail tambahan.
     - Low Level Design (LLD)
       Menjelaskan lebih detail tentang arsitektur suatu komponen, protocol yang digunakan untuk berkomunikasi, class yang dibutuhkan dan aspek desain lainnya.
       
3. Implementation
   - Fase ngoding
   - Berdasarkan HLD dan LLD
   - Membuat test plan
   
4. Testing
   - Menginstall code hasil implementation pada test environment
   - Testing berdasarkan test plan dokument yang berisi tentang list test yang menguji fitur dan fungsional dari software yang dispesifikkan dari costumer requirements.
   - Selain itu juga dilakukan integration testing, security testing, dan perfomance testing.
   - Jika ada yang tidak lolos tes, maka akan dilakukan fixing bugs oleh developer hingga code telah lulus test.
   
5. Deployment
   - Software akan diinstal di production environment.
   - Jika tidak ada masalah software akan dideliver ke costumer.
   
6. Maintenance
   - Memberikan suport kepada costumer.
   - Memperbaiki bug yang ditemukan.
   - Melakukan software improvement.
   - Gather permintaan baru dari costumer.

### Metode software development
#### Waterfall

- Metode ini menggunakan fase sdlc dengan kaku, harus berurutan dari 1 hingga 6, tidak kembali ke fase sebelumnya. 
- Suatu fase menunggu output dari fase sebelumnya sebagai input fasenya.
- Akan banya cost dan delay jika terjadi perubahan-perubahan.
    
#### Agile
Metode ini flexibel dan berfokus pada costumer.

- Agile Method
  - Agile Scrum
    Berfokus pada tim kecil yang diorganisasikan sendiri, melakukan pertemuan singkat setiap hari dan bekerja secara sprint yang berulang, terus menerus melakukan penyesuaian untuk requirement yang berubah. 
    - Sprint
      Ada banyak quick iterasi SDLC yang digunakan pada Agile untuk menyelesaikan frequent delivery of working software principle of the Agile manifesto.
    - Backlog
      Backlog berisi semua fitur software dalam bentuk list yang berprioritas. Berasal dari fase requirement dan analisis. Termasuk fitur yang belum dirilis.
    - User stories
      Statement simple dari keinginan user dan mengapa.
    - Scrum Teams
      - Tim scrum adalah cross-functional, collaborative, self-managed and self-empowered. Idealnya tidak lebih dari 10 orang namun dapat menyelesaikan satu user story dalam sekali sprint.
      - Setiap hari melakukan standup meeting yang tidak lebih dari 15 menit untuk menjaga semua anggota tim syncron dari apa yang sudah diselesaikan pada standup sebelumnya dengan apa yang akan dikerjakan hingga standup berikutnya, dan kendala apa yang menghambat mereka dalam menyelesaikan tugas.
  - Lean
    Menekankan pada penghapusan usaha yang sia-sia dalam perencanaan dan pelaksanaan, dan mengurangi beban kognitif programmer.
  - Extreme Programing
    Bersifat lebih prespektif terhadap best-practice software engineering, dan lebih menangani quality of life tertentu yang dihadapi tim software development.
  - Feature-Driven Development
    Pengembangan software harus diproses dalam kerangka model keseluruhan, dipecah, direncanakan, dirancang, dan dibangun fitur demi fitur. 

#### Lean
Meminimalkan waste dan memaksimalkan nilai kepada costumer.

- 7 waste software development
  - Partialy done work
    Karena tidak menambah value kepada costumer, waktu dan resource yang dipakai seharusnya bisa digunakan untuk memberikan value kepada costumer, biasanya tidak dimaintain.
  - Extra process
  - Extra features
    Jangan membuat sesuatu yang tidak diminta.
  - Task switching
    Perlu waktu untuk menyesuaikan diri ketika berpindah pekerjaan, oleh karena itu jangan banyak task switching.
  - Waiting
    Delay is waste.
  - Motion
    Pergerakan dan perpindahan untuk melakukan sesuatu yang dibutuhkan juga memakan waktu. 
  - Defects
    bug is waste.
- Perkuat pembelajaran dengan short sprint
  - developer akan belajar dengan cepat
  - customer dapat meberikan feedback dengan cepat
  - fitur dapat disesuaikan dan memberikan value kepada costumer
- Decide selambat mungkin
  - Jika ada ketidakpastian, tetap berpegang teguh pada fakta dibanding opini
  - Jika ada ketidakpastian, software dibuat seflexsibel mungkin agar dapat dilakukan perubahan nanti.
- Deliver secepat mungkin
- Berdayakan tim
  Setiap orang memiliki keahlian masing-masing berikan mereka keluasan untuk mengerjakan bidang yang mereka ahlikan. 
- Build integrity in
- Optimasi seluruhnya


## Software Design Patern
Menggunakan software design patern telah terbukti berhasi, menggunakannya akan meningkatkan kecepatan dalam mengembangkan perangkat lunak, karena tidak perlu mencari solusi-solusi baru cukup mengikuti patern saja.

### Original Design Patern
- Creational, digunakan untuk memandu, menyederhanakan, mengabstraksi software objek creation dalam skala besar. 
- Structural, patern menjelaskan cara yang dapat diandalkan dalam membuat objek dan class pada berbagai jenis projek perangkat lunak.
- Behavioral, merinci bagaimana objek dapat berkomunikasi dan bekerjasama dalam menghadapin tantang yang familiar dalam software engineering.

### Common Used Design Patern
- Observer Design Patern
  - Merupakan design notifikasi langgan yang membuat suatu objek(observer) menerima event ketika ada perbuhana pada objek(subject) yang mereka amati. Seperti pada notif social media.
  - Syarat:
    - Subjek memiliki kemampuan untuk menyimpan list observer
    - Subjek memiliki method untuk menambah dan menghapus observer
    - Semua observer harus mengimplementasikan callback to invoke ketika subje mengirimkan notif.
  - Kelebihannya adalah observer dapat menerima perubahan dari subjek secara realtime dan menyediakan better performance.

- Model View Controller (MVC)

## Version Control Systems
## Coding Basics
## Code Review and Testing
## Data Formats
