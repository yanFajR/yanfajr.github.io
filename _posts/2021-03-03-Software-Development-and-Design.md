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
   -
5. Deployment
   - Software akan diinstal di production environment.
   - Jika tidak ada masalah software akan dideliver ke costumer.
   
6. Maintenance
   - Memberikan suport kepada costumer.
   - Memperbaiki bug yang ditemukan.
   - Melakukan software improvement.
   - Gather permintaan baru dari costumer.

### metode software development
- Waterfall
    - Metode ini menggunakan fase sdlc dengan kaku, harus berurutan dari 1 hingga 6, tidak kembali ke fase sebelumnya. 
    - Suatu fase menunggu output dari fase sebelumnya sebagai input fasenya.
    - Akan banya cost dan delay jika terjadi perubahan-perubahan.
    
- Agile
Metode ini flexibel dan berfokus pada costumer.

- Lean


## Software Design Patern
## Version Control Systems
## Coding Basics
## Code Review and Testing
## Data Formats
