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

``` 
    mysql -u root
```

Perintah tersebut digunakan jika Anda menggunakan user root dan tanpa password, namun jika sudah memberi password pada akun user MySQL yang digunakan adalah perintah :

``` 
    mysql -u root -p
```

![Gambar 1](/images/mysql/1.png)

![Gambar 2](/images/mysql/2.png)

### Melihat Database, Create Database
Melihat database apa saja yang tersedia di dalam dapat menggunakan perintah :

``` 
    SHOW DATABASES;
```

_**Note :** Biasakan walau tidak wajib untuk menulis perintah pada command line MySQL dengan huruf UPPERCASE, ini untuk memnudahkan agar kita dapat membedakan mana perintah dan mana nama database/tabel/field yang kita buat._

![Gambar 3](/images/mysql/3.png)

Membuat (Create) Database, untuk membuat database, pastikan dahulu apakah database yang akan kita buat memiliki nama yang sama dengan database yang ada dengan perintah yang kita coba di atas tadi. Untuk membuat database kita bisa menggunakan perintah :

``` 
    CREATE DATABASE nama_database;
```

Pada gambar ini kita menamai database dengan nama "LaporanUjian".

![Gambar 4](/images/mysql/4.png)

Jika berhasil menambahkan maka ada output _Query OK_, selanjutnya kita cek dengan perintah _SHOW DATABASES;_ untuk memastikan benar berhasil.

![Gambar 5](/images/mysql/5.png)

### Menggunakan Database Tertentu

Kita akan mencoba menggunakan salah satu database yang ada, caranya yaitu menggunakan perintah :

```
    USE nama_database;
```

Dalam gambar ini kita menggunakan database dengan nama "LaporanUjian".

![Gambar 6](/images/mysql/6.png)

### Melihat Daftar Tabel, Membuat Tabel, Melihat isi Tabel

Setelah memilih database tertentu yang akan kita gunakan, langkah selanjutnya yang disarankan adalah melihat isi dari database tersebut, apakah tersedia atau tidak tabel yang akan digunakan, cara melihat daftar tabel adalah dengan perintah :

```
    SHOW TABLES;
```

![Gambar 7](/images/mysql/7.png)

Pada gambar tersebut, kita masih menggunakan database "LaporanUjian" dan di database tersebut masih belum memiliki tabel, sehingga jika kita ingin menambah tabel kita dapat menggunakan perintah :

```
    CREATE TABLE nama_tabel(nama_field1 TIPE_DATA(VALUE) PRIMARY KEY, namafield2 TIPE_DATA(VALUE) NOT NULL, ... , namafieldterakhir TIPE_DATA(VALUE) NOT NULL);
```

_**Keterangan :** Kita dapat memberikan atau tidak PRIMARY KEY pada nama field yang kita gunakan, keterangan lebih lengkap tentang tipe data dapat dilihat di [http://dev.mysql.com/doc/refman/5.7/en/data-types.html](http://dev.mysql.com/doc/refman/5.7/en/data-types.html)._

![Gambar 8](/images/mysql/8.png)

Pada gambar, kita menggunakan nama tabel "PesertaUjian".

Status _Query OK_ menandakan kita berhasil menambah tabel beserta field di dalamnya, kita cek apakah tabel benar telah ditambahkan pada database "LaporanUjian" dengan perintah _SHOW TABLES_ yang kita bahas sebelumnya.

![Gambar 10](/images/mysql/10.png)

Jika kita ingin melihat field dari tabel gunakan perintah :

```
    DESCRIBE nama_tabel;
```

_**Note :** perintah DESCRIBE dapat juga ditulis dengan DESC untuk mempersingkat pengetikan._

![Gambar 9](/images/mysql/9.png)

![Gambar 11](/images/mysql/11.png)

![Gambar 12](/images/mysql/12.png)

### Melihat dan Menambahkan Isi Data dari Field pada Tabel Tertentu

Melihat isi data pada field dalam tabel tertentu menggunakan perintah :

```
    SELECT * FROM nama_tabel;
```

![Gambar 13](/images/mysql/13.png)

Pada gambar tersebut kita menggunakan tabel "PesertaUjian", terlihat pada tabel tersebut field yang kita buat tadi masih belum ada data apapun. Kita dapat menambah data dengan perintah :


```
    INSERT INTO nama_tabel VALUE('isi field1','isi field2',...,'isi field terakhir');
```

_**Note :** Ada beberapa pilihan alternatif perintah INSERT untuk menambah data pada field, bisa dilihat pada [http://dev.mysql.com/doc/refman/5.7/en/insert.html](http://dev.mysql.com/doc/refman/5.7/en/insert.html) untuk referensi lebih lanjut._

![Gambar 14](/images/mysql/14.png)

Pada gambar tersebut kita menggunakan tabel "PesertaUjian" dan mendapat output _Query OK_ data yang kita masukkan berhasil ter_record_, untuk melihatnya kita gunakan perintah _SELECT * FROM_.

![Gambar 15](/images/mysql/15.png)

![Gambar 16](/images/mysql/16.png)

![Gambar 17](/images/mysql/17.png)

![Gambar 18](/images/mysql/18.png)






_**Referensi :**_

_[http://dev.mysql.com/doc/](http://dev.mysql.com/doc/)_