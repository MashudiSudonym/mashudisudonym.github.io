---
layout: post
title:  "Tugas ~ MySQL Koneksi dengan Database, Menambah Database, Tabel, Field, dan Data Field"
date:   2015-12-12 21:31:51
categories: tugas mysql database
comments: true
---

# Tugas ~ MySQL Koneksi dengan Database, Menambah Database, Tabel, Field, dan Data Field

Command MySQL pada catatan ini menggunakan XAMPP pada sistem operasi berbasis GNU/Linux (contoh : ./opt/lampp/bin/mysql), untuk cara memanggil command MySQL gunakan penyesuaian sesuai dengan sistem operasi yang Anda gunakan, dan atribut perintah mysql tetap sama pada sistem operasi apapun.

### MySQL Command Line
Masuk ke dalam MySQL Command Line dapat menggunakan perintah :

``` mysql
    mysql -u root
```

Perintah tersebut digunakan jika Anda menggunakan user root dan tanpa password, namun jika sudah memberi password pada akun user MySQL yang digunakan adalah perintah :

``` mysql
    mysql -u root -p
```

![Gambar 1](/images/mysql/1.png)

![Gambar 2](/images/mysql/2.png)

### Melihat Database, Create Database
Melihat database apa saja yang tersedia di dalam dapat menggunakan perintah :

``` mysql
    SHOW DATABASES;
```

_**Note :** Biasakan walau tidak wajib untuk menulis perintah pada command line MySQL dengan huruf UPPERCASE, ini untuk memnudahkan agar kita dapat membedakan mana perintah dan mana nama database/tabel/field yang kita buat_

![Gambar 3](/images/mysql/3.png)

Membuat (Create) Database, untuk membuat database, pastikan dahulu apakah database yang akan kita buat memiliki nama yang sama dengan database yang ada dengan perintah yang kita coba di atas tadi. Untuk membuat database kita bisa menggunakan perintah :

``` mysql
    CREATE DATABASE nama_database;
```

Pada gambar ini kita menamai database dengan nama "LaporanUjian".

![Gambar 4](/images/mysql/4.png)

Jika berhasil menambahkan maka ada output _Query OK_, selanjutnya kita cek dengan perintah _SHOW DATABASES;_ untuk memastikan benar berhasil.

![Gambar 5](/images/mysql/5.png)

