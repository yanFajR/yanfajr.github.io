---
published: true
layout: post
categories:
  - Networking
---
## Pengertian

- Jaringan komputer dua buah atau lebih komputer yang saling terhubung melalui sebuah media untuk saling bertukar resource.

- Dua buah komputer yang saling terhubung dengan 1 kabel sudah dapat dikatakan computer network. untuk dapat terhubung ke network komputer harus memiliki network interface card (NIC).

- Ada banyak cara untuk membentuk jaringan komputer, salah satu yang umum adalah LAN
  - IEEE 802.3 ethernet
  - IEEE 802.11 wireless
  
- Protokol suite
  - TCP/IP
  - OSI
  - Apple Talk
  - Novell NetWare
  
- **TCP/IP Layer**
  - **Application** (data)
    - Komunikasi diantara application programs
    - FTP, POP3, HTTP, WWW, DHCP, DNS, SNMP, TELNET, etc.
  - **Transport** (segment)
    - Komunikasi diatara processes.
    - UDP : Fast transmission
    - TCP : Reliable transmission
  - **Internet** (packet)
    - Komunikasi diantara hosts/Path delivery.
    - IP
  - **Data link** (frame)
    - Komunikasi diantara neighbor/one-hop delivery.
    - Berbeda jenis link physical maka beda protocol.
    - Contoh : PPP, 802.11, Ethernet, PPPoE.
  - **Physical** (bits)
    - wired
      - Twister pair
        - Fast LANS
        - 10 - 10 Gbps
      - Coaxial cable
        - Home broadband access
        - 10 Mbps
      - Fiber
        - core network
        - 100 Gbps
    - wireless
      - 5G
        - cellular access
        - 20 Gbps
      - WI-FI (
        - 802.11 a/b/g/n/ac/ax
        - 9.6 Gbps
  
- Plan of a router
  - manangement
    - contoh ssh, snmp
  - control
    - routing table
  - data
    - switching packet

- Jaringan komputer tidak terlepas dari perangkat-perangkat yang menyertainya.
  - end device, berperan sebagai perangkat yang digunakan pengguna. contoh : komputer, laptop, smartphone, printer, dll.
  - intermediary, berperan dalam pengiriman infomasi dari sumber ke tujuan. contoh : router, switch, access point, firewall.

- Komunikasi diantara host dapat dibedakan menjadi :
  - Unicast, satu host tepat ke satu host lainnya
  - Multicast, satu host ke beberapa host tertentu
  - Broadcast, satu host ke semua host 
  
- Hub digunakan untuk mengkoneksikan dua atau lebih host dalam satu network, tetapi hub memiliki kelemahan yaitu ia akan membroadcast pesan yang diterima dari satu host ke host lainnya walaupun maksud pesan tersebut ditujukan untuk satu host, dan juga hub hanya memiliki satu collision domain sehingga ketika dua host mengirim pesan secara bersamaan maka akan terjadi tabrakan yang menyebabkan penurunan kualitas jaringan.

- Switch muncul untuk mengatasi problem dari hub, dengan memisahkan colission domain pada tiap portnya.

### IPV6
- menyediakan end to end security
- qos
- global unique address

- type
  - unicast
  - multicast 
  - loopback 
  - unspecified
