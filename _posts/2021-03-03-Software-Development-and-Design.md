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
- **Creational**, digunakan untuk memandu, menyederhanakan, mengabstraksi software objek creation dalam skala besar. 
- **Structural**, patern menjelaskan cara yang dapat diandalkan dalam membuat objek dan class pada berbagai jenis projek perangkat lunak.
- **Behavioral**, merinci bagaimana objek dapat berkomunikasi dan bekerjasama dalam menghadapin tantang yang familiar dalam software engineering.

### Common Used Design Patern
- Observer Design Patern
  - Merupakan design notifikasi langgan yang membuat suatu objek(observer) menerima event ketika ada perbuhana pada objek(subject) yang mereka amati. Seperti pada notif social media.
  - Syarat:
    - Subjek memiliki kemampuan untuk menyimpan list observer
    - Subjek memiliki method untuk menambah dan menghapus observer
    - Semua observer harus mengimplementasikan callback to invoke ketika subje mengirimkan notif.
  - Cara kerja
    1. Observer menambahkan dirinya ke list obeserver milik subject
    2. Subject melakukan method untuk mengirimkan notif ketika ada perubahan
    3. Observer menerima notif dari subject
  - Kelebihannya adalah observer dapat menerima perubahan dari subjek secara realtime dan menyediakan better performance.

- Model View Controller (MVC)
  - Dapat dipertimbankga sebagai arsitektural design patern, menyimpelkan pengembangan perangkat lunak berbasis gui. 
  - Komponen:
    - Model
    
      Model merupakan struktur data aplikasi yang bertanggung jawab untuk mengelola data, logic, dan rule aplikasi. Model mendapat input dari controller. 
    - View
    
      Visual representation dari data.
    - Controller
    
      Penengah dari model dan view, controller mengambil input dari user lalu memanipulasinya menjadi format yang dapat dimengerti model.
  - Cara kerja
    1. User memberi input ke controller
    2. Controller memanipulasi input menjadi format yang dapat dimengerti ke model
    3. Model mengolah dan mengupdate data ke view
    4. View menampilkan visual output data ke user.
  - Kelebihannya adalha masing-masing komponen dapat dibangun secara paralel dan masing-masing komponen dependen.
    
## Version Control Systems
- Version control adalah bagaimana untuk mengelola perubahan pada set file dengan cara berurutan dan menjaga histori perubahannya. 
- Pada version control menyimpan master file dan histori perubahan pada sebuah repo, jika seseorang ingin melakukan perubahan ia harus membuat working copy dari repo tersebut agar tidak mempengaruhi yang lain.
- Manfaat Version Control
  - Memungkinkan kolaborasi
  - Akuntabilitas dan visibilitas
  - Work in isolation
  - Aman
  - Bekerja dimanapun
  
### Tipe version control
- Local/LVCS
  - File dan version database pada local.
- Centralized/CVCS
  - FIle pada local, dan version database pada sistem terpusat.
  - Hanya 1 user berkerja pada satu file secara bersamaan. pake kunci mencegah user lain juga berkerja pada file yang sama.
- Distributed/DVCS
  - yang banyak digunakan, ketika mau mengubah harus clone dari hosting repo, bisa banyak user bekerja pada file yang sama karena bekerja dengan working copy masing-masing.
  
### Git
- Git adalah impelementasi dari distributed version control system yang open-source dan sudah terkenal didalam dunia software.
- Cara kerja git berbeda dengan version control lainnya, git menggunakan snapshot.
- Git stage:
  - Repository .git
    - Menyimpan files (compressed), commits, and logs (commit history).
  - Staging area
    - Menyimpan apa yang ingin ditambahkan, diedit, dihapus oleh user.
  - Working Directory
- 3 State
  - Commited -> disimpan ke repo .
  - Modified -> perubahan pada working directory
  - Staged   -> disimpan pada staging area.
  
### Local Vs Remote Repo
- Local
  - client machine
- Remote
  - Hosting service
  
### Branch
- Memungkinkan client bekerja secara independent tanpa mempengaruhi client lain.

### Github
- Pull request adalah cara kontributor untuk meminta new code, edits to existing code, dll.

### Git Commands
- Setup
```
git config --global user.name "<user's name>"
git config --global user.email "<user's email>"
```
- Membuat repo
```
git init <project directory>
```
- Clone repo
```
git clone <repository> [target directory]
```
- Melihat perubahan pada working directory
```
git status
```
- Membandingkan perubahan diatara dua file
```
git diff <file path>
git diff <commit id> <file path>
git diff <commit id 1> <commit id 2> <file path>
git diff <file path 1> <file path 2>
```
- Menambah file pada stagging area
```
git add <file path>
git add .
```
- Menghapus file pada repo
```
git rm <file path 1> ... <file path n>
git rm --cached <file path 1> ... <file path n>
```
- Memperbaharui repo
```
git commit
git commit -m "<message>"
```
- Memperbaharui remote repo
```
git push origin <branch name>
```
- Mendapatakan pembaharuan ke local
```
git pull
git pull origin
git pull origin <branch>
```
- Brancing
```
git branch <parent branch> <branch name>
git checkout -b <parent branch> <branch name>
```
- Menghapus branch
```
git branch -d <branch name>
```
- Mendapatkan list brancH
```
git branch
git branch --list
```
- Merge branch
```
git merge <branch name>
```
Berpindah ke branch lain
```
git checkout <target branch name>
```

### .diff File
Menunjukkan perbedaan dua versi dari sebuah file.
- + : Menunjukkan baris yang ditambah
- - : Menunjukkan barus yang dihapus
- /dev/null : Menunjukkan apakah file sudah dihapus atau ditambahkan.
- or "blank": Gives context lines around changed lines.
- @@ : A visual indicator that the next block of information is starting. Within the changes for one file, there may be multiple.
- index : Menampilkan perbandingan commit

```
diff --git a/file1 b/file2
```
  
## Coding Basics
### Methode, Function, Modules, dan Classes
Membantu membuat code menjadi lebih baik, dan mudah untuk dikolaborasikan.

- Methode and Function
  - Perbedaan methode adalah methode merupakan bagian dari object. 
  - Arguments -> nilai yang dikirimkan
  - Parameters -> variable pada function
  - Return Statements -> Nilai yang dihasilkan
  
  Function
  ```
  # Define the function
  def functionName:
  	...blocks of code...
    
  # Call the function
  functionName()
  ```
  Method
  ```
  # Define the class
  class className
  	# Define amethod
    def method1Name
    	...blocks of code
    # Define anothermethod
    def method2Name
    	...blocks of code
    # Define yet anothermethod
    def method3Name
    	...blocks of code
  
  #Instantiate the class
  myClass = className()
  #Call the instantiation and associated methods
  myClass.method1Name()
  myClass.method2Name()
  myClass.method3Name()
  ```
  
- Modules
  - seperti menggunakan library eksternal, kita juga bisa membuatnya sendiri dari file terpisah.
- Classes
  - akrab dengan konsep oop

### Clean Code
- Kode yang mudah dibaca dan dimengerti oleh developer lain

## Code Review and Testing
- Goal Final Code
  - Mudah dibaca
  - Mudah dimengerti
  - Mengikuti coding best practices
  - Menggunakan correct formatting
  - Free of bugs
  - Punya proper comments and documentation
  - Clean
  
- Tipe Code reviews
  - Formal Code Review
    - Melakukan beberapa meeting untuk melakukan pengriviewan
  - Changed-Based Code Review
  - Over-The-Shoulder Code Review
    - Memungkinkan fix bug on the spot.
  - Email Pass-Around
  
- Testing Framework
  - unittest
  - PyTest
  
- Unit test
  Test pada unit seperti class, methode, module, class.
- Integration test

## Data Formats
### XML
- Extensible Markup Language
- Cikal bakal HTML
- Menggunakan tag-tag
- Contoh
```
<?xml version="1.0" encoding="UTF-8"?>
<!-- Instance list -->
<vms>
  <vm>
    <vmid>0101af9811012</vmid>
    <type>t1.nano</type>
  </vm>
  <vm>
    <vmid>0102bg8908023</vmid>
    <type>t1.micro</type>
  </vm>
</vms>
```
- user-defined tag name

### JSON
- JavaScript Object Nation
- Contoh
```
{
  "edit-config":
  {
    "default-operation": "merge",
    "test-operation": "set",
    "some-integers": [2,3,5,7,9],
    "a-boolean": true,
    "more-numbers": [2.25E+2,-1.0735],
  }
}
```

### YAML
- YANL Aint Markup Language
- Mirip json, tetapi dalam beberapa kasus lebih baik dibanding json
- Contoh
```
---
edit-config:
  a-boolean: true
  default-operation: merge
  more-numbers:
  - 225.0
  - -1.0735
  some-integers:
  - 2
  - 3
  - 5
  - 7
  - 9
  test-operation: set
...
```

### Parsing and Serialisasi
- Pengubahan dalam bentuk yang bisa dikirim dan bisa dimengerti kembali.
- Parsing xml

```
import xml.etree.ElementTree as ET
import re

xml = ET.parse("myfile.xml")
root = xml.getroot()

ns = re.match('{.*}', root.tag).group(0)
editconf = root.find("{}edit-config".format(ns))
defop = editconf.find("{}default-operation".format(ns))
testop = editconf.find("{}test-option".format(ns))

print("The default-operation contains: {}".format(defop.text))
print("The test-option contains: {}".format(testop.text))

```

- Parsing JSON

```
import json
import yaml

with open('myfile.json','r') as json_file:
    ourjson = json.load(json_file)
print(ourjson)
print("\n\n---")
print(yaml.dump(ourjson))

print("The access token is: {}".format(ourjson['access_token']))
print("The token expires in {} seconds.".format(ourjson['expires_in']))

```

- Parsing YAML

```
import json
import yaml
with open('myfile.yaml','r') as yaml_file:
    ouryaml = yaml.safe_load(yaml_file)

print(ouryaml)
print("\n\n")
print(json.dumps(ouryaml, indent=4))

print("The access token is {}".format(ouryaml['access_token']))
print("The token expires in {} seconds.".format(ouryaml['expires_in']))
```
