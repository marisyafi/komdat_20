#### Kelompok 20 

| Nama | NIM |
|--------|--------|
| Marisya Fitri Islamy  |   G64140020     |
| Marchelia Fika Pratiwi  |   G64140048     |
| Amalia Rizkia Dayani  |   G64140064    |
|Nabila Sekar Ramadhanti   |   G64140094     |

# Aplikasi Web "Shaarli"

## Sekilas Tentang Shaarli
Shaarli adalah salah satu situs *web bookmarking service* yang menyediakan layanan untuk menyimpan dan berbagi link dengan mudah. Situs ini tidak menggunakan database sehingga dapat digunakan dengan mudah dan cepat. Sederhana tapi performanya cukup bagus untuk digunakan. Data yang dimasukkan tidak di *hosting* di server asing melainkan melalui server pribadi.


## Instalasi
Untuk melakukan instalasi Shaarli pada *virtual private server* (VPS) diperlukan beberapa *requirement* diantaranya adalah:

**Software Requirement:**
1. Install Apache, MySQL, PHP
1.  Install Composer
1.  Install Shaarli
1. Install Composer ke Shaarli

**Server Requirements:**
1. Linux/FreeBSD/Windows OS server platform
1. Apache 1.3 or above (mod_rewrite module installed)
1. MySQL 5.2+
1. PHP 5.3.6+ (GD lib, XML lib, FreeType installed)

Berikut cara menginstal aplikasi web “Shaarli” pada* virtual private server* (VPS) berbasis Linux pada CLI:

#### Instal Apache, MySQL, PHP

```
$ sudo apt install apache2
$ sudo apt install mysql-server
$ sudo apt install php
$ sudo apt install libapache2-mod-php
$ sudo apt install php-mysql
$ sudo apt install php-gd php-mcrypt php-mbstring php-xml php-ssh2
$ sudo service apache2 restart
```

#### Instal Composer
```
$ sudo apt-get install curl php5-cli git
$ curl -s https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
```


#### Install Shaarli

```
$ wget https://github.com/shaarli/Shaarli/releases/download/v0.8.4/shaarli-v0.8.4-full.zip
$ unzip shaarli-v0.8.4-full.zip
$ mv Shaarli /path/to/shaarli/
```

#### Install Composer ke Shaarli
```
$ cd /path/to/shaarli/
$ composer install
```




##  Maintenance

Backup file `data/datastore.php` (by FTP or SSH). Untuk mengembalikan data sebelumnya ke file sebelumnya.

Contoh command:
```
$ rsync -avzP my.server.com:/var/www/shaarli/data/datastore.php datastore-$(date +%Y-%m-%d_%H%M).php
```





## Cara Pemakaian

- Tampilan aplikasi web

**Tampilan Home**
![](http://1.bp.blogspot.com/-Ets4-uR9GTk/WODerPC-i4I/AAAAAAAACrM/Jl9tvADTseoZWMBttEVvCeOz22fBsgZVwCK4B/s1600/home.png)


**Tampilan Daily**
![](http://2.bp.blogspot.com/-pxQIxvEfpK0/WODevCKPz3I/AAAAAAAACrU/8ZmHZZ_Jm30CVnd91u2T3so0WQZX-At6QCK4B/s1600/daily.png)


**Tampilan Add Link**
![](http://4.bp.blogspot.com/-4qYckPXehHY/WODeq91OLxI/AAAAAAAACrE/7xv7ws6CMuo7b4HlqrbKsoqZ-UTsLgxjACK4B/s1600/add%2Blink.png)



- Fungsi-fungsi utama

Menambahkan Link

Kita dapat dengan mudah menambahkan link yang ingin kita share di Shaarli, cukup dengan membuka halaman “Add Link”.  Lalu menambahkan link yang ingin disimpan atau di share dan klik button Add link.

![](http://3.bp.blogspot.com/-F0CDg_q_KpI/WODeqHSkkFI/AAAAAAAACqs/KmFVtc5r1R8rLnuqME8KlaOSkdgT9FDLgCK4B/s1600/4.png)

Setelah klik button Add link kita dapat menambahkan deskripsi mengenai link yang kita tambahkan.

![](http://4.bp.blogspot.com/-evpFPMDKOjk/WODeql5fjII/AAAAAAAACq0/p_NL0eASG4MeZGN8Ir8G4rMugBsAQ2kcACK4B/s1600/5.png)

Tampilan setelah di publish

![](http://2.bp.blogspot.com/-mHgRwUIeZZA/WODeq6cgkXI/AAAAAAAACq8/AfOyLmbGfMAycWN3KoeineVFTxf5JvVngCK4B/s1600/6.png)


## Pembahasan

**- Pendapat kami tentang aplikasi web ini**
  
| Kelebihan:  | Kekurangan: |
|--------|--------|
|    Minimalist Design    |Tampilannya kurang menarik        |
|  Tidak dapat dilacak oleh *addons browser *  |  -  | 
|    Dapat menyimpan banyak link   |  -|
|     Dapat mengakses data tanpa harus login    |    -    |
|Lebih cepat daripada kebanyakan layanan bookmark|-|
|Tag renaming, merging and deletion|-|
|Link pribadi Anda tidak dihosting di server pihak ketiga.|-|
|Data adalah milikmu, host pada server Anda|-|


**- Perbandingkan dengan aplikasi web  sejenis**

| Kategori|Shaarli | Diigo |
|--------|--------|--------|
|Addons Browser|Anda tidak dilacak oleh addons browser|Anda dapat dilacak oleh addons browser|
|Database| Sangat cepat karena tidak menggunakan real database|Real database|
|Available Device|Mobile Apps, Web Based|Mobile Apps, Web Based|
|Highlight| Tidak ada fitur highlight | Ada fitur highlight|
|Gmail *sign in*| Tidak bisa *sign in* menggunakan gmail| Bisa *sign in* menggunakan gmail|
|Grup|Tidak ada fitur membuat grup atau kelompok kecil| Terdapat grup dan bisa share link ke grup tersebut
|Penanda|Tidak ada fitur penanda | Add text, comment and reminders dalam web page dengan *sticky notes* 



## Referensi

https://github.com/shaarli/Shaarli

https://github.com/shaarli/Shaarli/wiki/FAQ

https://shaarlidemo.tuxfamily.org/

https://www.diigo.com/

