---
layout: post
title:  "Tugas ~ Sistem File Linux"
date:   2015-04-17 16:31:51
categories: tugas linux open source
comments: true
---
Pada ringkasan materi ini akan membahas tentang dasar teori dari :

- Atribut File
- Ijin Akses
- User Mask

# 1. **Atribut File**
File memiliki beberapa atribut antara lain :

- **Tipe File** 	:	
Menentukan tipe dari file, yaitu :


![Gambar 1](/images/1.png)


- **Ijin Akses** 	:	
Menentukan hak user terhadap file.

- **Jumlah Link** 	:	
Jumlah link untuk file.

- **Pemilik (owner)** 	:	
Menentukan siapa pemilik file.

- **Group** 	:	
Menentukan group yang memiliki file.

- **Jumlah Karakter** 	:	
Menentikan ukuran file dalam byte.

- **Waktu Pembuatan** 	:	
Menentukan kapan file terakhir dimodifikasi.

- **Nama File** 	:	
Menentukan nama file yang dimaksud.


Contoh :
![Gambar 2](/images/2.png)


# 2. **Ijin Akses**

Setiap obyek pada Linux harus mempunyai pemilik, yaitu nama pemakai *(account)* yang terdaftar pada */etc/passwd.*

Ijin akses dibagi menjadi 3 yaitu:

- Pemilik (Owner)
- Kelompok (Group)
- Lainnya (Others)

Setiap peran dapat melakukan 3 bentuk operasi yaitu :

- **Pada File**
	- R (Read) 		: Ijin untuk membaca.
	- W (Write) 	: Ijin untuk mengubah/membuat.
	- X (Execute) 	: Ijin untuk menjalankan program.

- **Pada Direktori**
	- R (Read) 		: Ijin untuk membaca daftar file dalam direktori.
	- W (Write) 	: Ijin untuk mengubah/membuat file di direktori.
	- X (Execute) 	: Ijin untuk masuk ke direktori *(cd).*

Pemilik file/direktori dapat mengubah ijin akses sebagai berikut :

![Gambar 3](/images/3.png)

Format untuk mengubah ijin akses

	chmod [ugoa] [= + -] [rwx] File(s)
	chmod [ugoa] [= + -] [rwx] Dir(s)

_**Keterangan :**_

	u = user (pemilik)
	g = group (kelompok)
	o = others (lainnya)
	a = all

*chmod* dapat pula menggunakan bilangan octal sebagai berikut :

	r 	w 	x
	4	2 	1 	=	7 <-- hasil dari bilangan oktal yang dijumlahkan

_**r**_ (read) dilambangkan _**4**_ dalam bilangan octal.

_**w**_ (write) dilambangkan _**2**_ dalam bilangan octal.

_**x**_ (execute) dilambangkan _**1**_ dalam bilangan octal.



# 3. **User Mask**

Contoh dalam penggunaan ijin akses pada poin 2 tadi adalah untuk menentukan ijin akses pada saat file atau direktori dibuat digunakan perintah _**umask**_. Untuk menghitung nilai default melalui _**umask**_ pada file, maka dapat dilakukan sebagai berikut :

	Kreasi file (biasa)		6 6 6
	Nilai umask			0 2 2
					----- -
					6 4 4

	Kreasi Direktori 		7 7 7
	Nilai umask 			0 2 2
					----- -
					7 5 5