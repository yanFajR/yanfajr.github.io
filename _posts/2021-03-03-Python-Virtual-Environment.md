---
published: false
layout: post
categories:
  - Python
---
Ketika kita ingin membuat program kita ingin package-package yang terinstall di environment kita adalah hanya yang dibutuhkan saja, namun kita menemukan sudah banyak package terinstall pada system kita. oleh karena itu kita bisa membuat virtual environment yang terpisah dan belum terinstall package apapun menggunakan *venv*.

Package manager pada python adalah pip/pip3.

### Membuat virtual environment
'''''
python3 -m venv envbaru
'''''

### Mengaktifkan virtual environment
'''''
source envbaru/bin/activate
'''''

### Cek package terinstall
'''''
pip3 freeze
'''''

### Install package
'''''
pip3 install requests
'''''

### Menonaktifkan virtual environment
'''''
deactivate
'''''

### Menyalin package virtual environment ke sebuah file text
'''''
pip3 freeze > requirements.txt
'''''

bisa menambahkan grep untuk mendapatkan yang lebih spesifik.

### Menginstall package dari file list package
'''''
pip3 install -r requirements.txt
'''''
