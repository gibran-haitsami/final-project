# Final_project OS Server 22.83.0831_Gibran Hait Sami 

Membuat webserver di ubuntu 22.04 menggunakan:
   - Apache2
   - ppmyadmin
     
Layanan service yang diinstall:
   - ssh
   - Ftp

Apache, adalah server web open-source yang populer dan digunakan secara luas di seluruh dunia. Dirancang untuk menyajikan halaman web dan sumber daya lainnya melalui protokol HTTP, Apache2 memiliki fleksibilitas tinggi, modularitas, dan mendukung banyak fitur keamanan. 

-install Apache 2
```bash
sudo apt-get update
```
```bash
sudo apt install apache2
```
```bash
sudo apt install php libapache2-mod-php php-mysql mysql-server
```
Jalankan apache2
```bash
sudo systemctl enable apache2
sudo systemctl start apache2
```
```bash
sudo systemctl status apache2
```
Install php my admin
``` bash
sudo apt install phpmyadmin
```
enable exkstensi php
```bash
sudo phpenmod string
```
restart service 
```bash
sudo systemctl restart apache2
```

untuk mengakses ke apache2 bisa mengetikkan di browser 'iplocalhost' dan
untuk mengakses phpmyadmin ketik di browser 'iplocalhost/phpmyadmin'

install dan konfigurasi ssh
```bash
sudo apt-get update
```

```bash
sudo apt install openssh-server
```

konfigurasi ssh 
```bash
sudo ufw allow ssh
```

```bash
sudo nano /etc/ssh/sshd_config
```

ubah port sesuai keinginan 
```bash
port 22
```
untuk mengecek status ssh
```bash
sudo systemctl status ssh
```
restart service ssh
```bash
sudo systemctl restart ssh
```
running di cmd
```bash
ssh -p 22 username@'iplocalhost'
```
![image](https://github.com/gibran-haitsami/final-project/assets/148223934/dd2e4453-5833-42b9-8fbc-8ea62b8de359)


install dan konfigurasi Ftp 
```bash
sudo apt install vsftpd
```
setelah itu backup 
```bash
sudo cp /etc/vsftpd.conf /etc/vsftpd.conf.orig
```
masuk konfigurasi ftp 
```
nano /etc/vsftpd.conf
```
seusaikan seperti dibawah ini:
```bash
write_enable=YES
```
anonymous_enable=NO
```
local_enable=YES
```














