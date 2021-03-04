---
published: true
---
Freeradius adalah open-source radius yang populer banyak digunakan oleh perusahaan.

## Install freeradius dan modul tambahannnya
  1. Update repo
     ```
     sudo yum -y update
     ```
  2. Cari free radius
     ```
     yum search all freeradius
     ```
  3. Install freeradius, utils, perl, dan mysql.
     ```
     yum -y install freeradius freeradius-utils freeradius-mysql freeradius-perl
     ```
  4. Jalankan dan enable free radius
     ```
     systemctl start radiusd.service
     systemctl enable radiusd.service
     ```
  5. Cek status radius service
     ```
     systemctl status radiusd.service
     ```
 
## Konfig firewall
untuk mengizinkan paket radius dan httpd melewati system.
  1. Install Firewalld
     ```
     yum install firewalld
     ```
  2. Disable SELinux, edit file /etc/selinux/config set
     ```
     SELINUX=disabled
     ```
  3. Enable, start, dan cek status firewalld
     ```
     systemctl enable firewalld
     systemctl start firewalld
     systemctl status firewalld
     ```
  4. Tambahkan rule untuk mengizinkan http, https, dan radius
     ```
     firewall-cmd --add-service={http,https,radius} --permanent
     ```
  5. Reload firewaal
     ```
     firewall-cmd --reload
     ```
  6. Confirm default-zone dan service diizinkan
     ```
     firewall-cmd --get-default-zone
     
     firewall-cmd --list-services --zone=public
     ```

## Testing radius
Menjalankan radius dalam mode debug, berhasil ketika "ready to process requests".
  ```
  pkill radiusd
  radiusd -X
  ```

## Konfig MariaDB
  1. install mariadb 10
     - Tambah repo file
       ```
       nano /etc/yum.repos.d/MariaDB.repo
       ```
       Tambahkan pada file tersebut
       ```
       [mariadb]
       name = MariaDB
       baseurl = http://yum.mariadb.org/10.1/centos7-amd64
       gpgkey=https://yum.mariadb.org/RPM-GPG-KEY-MariaDB
       gpgcheck=1
       ```
       ```
       yum -y update
       yum install -y mariadb-server mariadb
       ```
     - Jalankan mariadb
       ```
       systemctl start mariadb
       systemctl enable mariadb
       systemctl status mariadb
       systemctk is-eabled mariadb.service
       ```
  2. Amankan mariadb
     - set root password, remove anonymus user, dissalow root login remotely, remove test database, reload privilage table now.
       ```
       mysql_secure_installation
       ```

## Konfig PHP
  1. install php 7
     ```
     yum install epel-release yum-utils
     sudo yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm
     sudo yum-config-manager --enable remi-php73
     sudo yum install php php-common php-opcache php-mcrypt php-cli php-gd php-curl php-mysqlnd
     ```
  2. cek php version
     ```
     php -v
     ```

## Konfig freeradius menggunakan mariadb
  1. login mariadb
     ```
     mysql -u root -p
     ```
  2. buat database radius dan berikan akses ke user radius.
  
     perlu perhatian lebih pada  `radius`@localhost dan "`radiuspassword`" yang merupakan user dan password untuk mengaitkan database pada konfigurasi freeradius, dan DATABASE `radius` yang merupakan nama databasenya.
     ```
     CREATE DATABASE radius;
     GRANT ALL ON radius.* TO radius@localhost IDENTIFIED BY "radiuspassword";
     FLUSH PRIVILEGES;
     quit;
     ```
  3. Import skema radius database ke mariadb radius database
  
     YOUR_PASSWORD merupakan password root database saat menginstall secure mysql.
     ```
     mysql -uroot -pYOUR_PASSWORD radius < /etc/raddb/mods-config/sql/main/mysql/schema.sql
     ```
  4. Create a soft link  for SQL
     ```
     ln -s /etc/raddb/mods-available/sql /etc/raddb/mods-enabled/
     ```
  5. Konfigurasi freeradius server untuk menggunakan database server
     - ganti, driver = "rlm_sql_null" ke driver = "rlm_sql_mysql"
     - ganti, dialect = "sqlite" ke dialect = "mysql"
     - hapus # pada server, port, login, passwor, ganti dengan user database dan password database radius.
     - hapus # pada read_clients = yes
     ```
     nano /etc/raddb/mods-available/sql
     ```
  6. Ganti grup /etc/raddb/mods-enabled/sql ke radiusd
     ```
     chgrp -h radiusd /etc/raddb/mods-enabled/sql
     ```
  7. Testing radius mode debug kembali.

## Konfig GUI WebPanel
  1. install httpd server
     ```
     yum groupinstall "Development Tools" -y
     yum -y install httpd httpd-devel
     
     systemctl enable httpd
     systemctl start httpd
     systemctl status httpd
     ```
  2. Download daloRadius 
     ```
     wget https://github.com/lirantal/daloradius/archive/master.zip
     unzip master.zip
     mv daloradius-master/ daloradius 
     ```
  3. Tambahkan daloRadius SQL Schema
     ```
     cd daloradius
     mysql -u root -p radius < contrib/db/fr2-mysql-daloradius-and-freeradius.sql 
     mysql -u root -p radius < contrib/db/mysql-daloradius.sql
     ```
  4. Konfigurasi daloRadius DB opsi
     ```
     cd ..
     mv daloradius /var/www/html/

     chown -R apache:apache /var/www/html/daloradius/
     cd /var/www/html/daloradius/library/
     cp daloradius.conf.php.sample daloradius.conf.php
     chmod 664 /var/www/html/daloradius/library/daloradius.conf.php
     chmod 755 -R /var/www/html/daloradius/login.php
     ```
     Konfigurasi untuk daloradius
     ```
     vi /var/www/html/daloradius/library/daloradius.conf.php
     ```
     Ubah
     ```
     $configValues['CONFIG_DB_USER'] = 'radius';
     $configValues['CONFIG_DB_PASS'] = 'radiuspassword';
     $configValues['CONFIG_DB_NAME'] = 'radius';
     ```
     ```
     systemctl restart radiusd.service 
     systemctl restart mariadb.service 
     systemctl restart httpd
     ```
     ```
     yum install php-pear
     pear install DB
     ```
     
## Logging ke daloRadius
   - kunjungi http://your-server-ip-address/daloradius/login.php
     - username : administrator
     - password : radius
   - Pastikan bahwa status radius active
     ![active.PNG]({{site.baseurl}}/images/active.PNG)
     Jika tidak active
     ```
     pkill radiusd
     radiusd
     ```

## Install ke Mikrotik
  - Management > Nas > New Nas
    - ip mikrotik
  ![nas.PNG]({{site.baseurl}}/images/nas.PNG)
  ![portnas.PNG]({{site.baseurl}}/images/portnas.PNG)

  - Management > Users > New Users
  ![userrad.PNG]({{site.baseurl}}/images/userrad.PNG)
  
  - Winbox
    - ip server centos
  ![mikro.PNG]({{site.baseurl}}/images/mikro.PNG)
