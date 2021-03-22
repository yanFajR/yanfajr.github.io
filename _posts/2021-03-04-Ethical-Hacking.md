---
published: true
layout: post
categories:
  - Security
---
Materi yang berkaitan dengan Ethical hacking.

**Terminologi:**
- Hack Value
  
  Nilai yang menunjukkan sesuatu yang menarik untuk alasan hacking.
   
- Payload

  Bagian dari kode yang melakukan suatu action.
  
- Vulnerability

  Kerentanan pada suatu sistem.
  
- Exploit

  Pembobolan sistem dari vulnerability yang ada.
  
- Zero-Day Attack

  Serangan sebelum pengembang melakukan penambalan vulnerability.
  
- Daisy Chaining

  Mendapatkan akses ke suatu sistem.
  
- Bot

  Software yang melakukan perintah tertentu secara automatis.
  
- Doxing

  Mempublish informasi mengenai seseorang
  
## Elemen Keamanan Informasi
- Confidentialy
- Integrity
- Availiability
- Authenticity
  Memastikan keaslian.
- Non-repudiation
  Pengirim pesan tidak dapat mengelak bahwa ia yang mengirimkan pesan tersebut.
  
## Attack
- **Attack** terjadi karena adanya motive, methode, dan vulnerability

- Top vektor penyerangan keamanan informasi
  - Cloud computing threats
    - data loss
    - hijacking
  - Advanced presisten threats
  - Virus dan worms
  - Mobile threats
  - Insider attack
    - attack by trusted person
  - Botnets
  
- Kategori Ancaman
  - Network threats
    Information gathering, Sniffing, Spoofing, Session hijacking, MITM, Dns adn Arp Poinsoning, Passwod base attack, Dos, dll.
  - Host threats
    Malware attack, Password attack, privilege escalation, unauthorized acces, footprinting, dll.
  - Application threats
    Phising, SQL injecrion, Information disclosure, security misconfig, dll.
  
- Tipe Searangan
  - OS Attacks
    Mencari vulnerability suatu os.
    - buffer overvflow
    - bugs
    - unpatched os
    
  - Misconfiguration Attacks
    Kesalahan konfigurasi yang menyebabkan ilegal access.
  - App level attacks
    Mengeksploitasi vulnerability suatu aplikasi.
  - Shrink Wrap Code attacks
    Exploit default configuration.
    
## Hacking
- Melakukan eksploitasi terhadap suatu vulnerability sistem untuk mendapatkan access yang ilgal terhadap suatu resource pada sistem.
- Termasuk memodifikasi sistem/aplikasi dengan maksud tujuan tertentu.
- Hacker
  - Orang yang memiliki IT skill yang luar biasa
  - Seorang yang memiliki hoby dalam hacking
  - Orang yang sedang mencoba-coba untuk belajar
- Fase
  - Footprinting & Reconnaissance
    - Mencari informasi sebanyak mungkin mengenai target yang akan diserang.
    - Target : klien, pegawai, network, sistem operasi, dll.
    - Ada dua macam :
      - active
        Langsung berinteraksi dengan target.
      - passive
        Tidak berinteraksi langsung, dengan mencari public record.
    - Tujuan Footprinting
      - Mengetahui keamanan
      - Mengurangi fokus area
      - Mengidentifikasi vuln
      - Menggambar topologi network
    - Teknik Footprinting : Search engine, Advanced Google Hacking https://www.google.com/advanced_search , Social Network, Website, Email, WHOIS, DNS, Network, Social Engineering.
  - Scanning
    - Scan the network
  - Gaining Access
  - Maintaining Access
    - Backdor, rootkits, trojan
  - Clearing Tracks
  -
  
  
## Network Scanning

- Informasi dari footprinting digunakan untuk fase scanning network.

- Network scanning adalah  method untuk mendapatkan:
  - Live hosts pada sebuah network
  - open dan closed ports
  - informasi os
  - service yang running pada sebuah network
  - apakah ada device keamanan seperti firewall
  - arsitektur sebuah system
  - running service
  - mengidentidikasi vulnerabilities
  
- Scanning network termasuk menyelidiki(probing) target network untuk mendapatkan information

### TCP Communication
  - Flag adalah bagian dari tcp header:
    - SYN => untuk inisiasi tcp connection betwet two hosts.
    - ACK => memberitahu bahwa telah menerima paket.
    - URG => mengindikasikan bahwa data yang terkandung dalam paket itu penting dan harus diproses secepatnya.
    - PSH => menginstruksikan system untuk mengirim all buffered data secepatnya.
    - FIN => memberitahu remote system untuk end tcp connection.
    - RST => reset a connection.

### Scanning Metodologi
  - checking live system (host discovert)
    - menggunakan icmp echo request,jika ada reply maka host itu aktif
    - icmp scanning
    - ping sweep
  - menemukan open ports
    - ssdp(simple service discovery protocol) scanning
    - nmap
    - hping2 & hping3
  - scanning beyond ids
  - banner grabbing
  - scanning vulnerabilities
  - network diagram
  - proxies
  
### Scanning Techniques
- TCP Connect/Full Open Scan
- Stealth Scan (Half-open Scan)
- Inverse TCP Flag Scanning
