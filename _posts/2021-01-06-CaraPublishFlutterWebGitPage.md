---
layout: post
title:  "Cara Publish Flutter Web ke GitPage"
date:   2021-01-06 18:29:51
categories: Share, Tutorial, Flutter
comments: true
---

# Cara Publish Flutter Web ke GitPage

Langsung saya anggap sudah mengerti cara memulai projek flutter, memulai menjalankan projek flutter untuk web, dan konfigurasi-konfigurasi flutter lainnya.
Begitu juga untuk cara memulai sebuah GitPage.

Lakukan build ke versi web dari projek flutter yang sudah selesai dibuat dengan perintah :

```
    flutter build web
```

Hasil generate atau build akan tersimpan pada folder build dengan nama folder web. Selanjutnya copy - paste folder web tersebut ke dalam folder yang telah anda inisiasi sebagai project GitPage. Jika folder tadi menumpang ke GitPage yang sudah anda buat, dianjurkan mengubah nama folder web tadi dengan nama yang mudah anda mengerti.

![SusunanFolder](/images/flutter-web-gitpage/ss.png)

Pada gambar tersebut folder web yang saya maksud adalah folder bertanda kuning.

Untuk selanjutnya, buka folder tersebut dan buka file index.html. Jadikan komentar tag html berikut ini.

```
    <base href="/">
```

Menjadi seperti ini

Sebelum :

![Sebelum](/images/flutter-web-gitpage/ss2.png)

Sesudah :
![Sesudah](/images/flutter-web-gitpage/ss3.png)

Padahal tag tersebut hasil build dari flutter tapi kalau itu aktif di gitpage tidak bisa dibuka aplikasinya.

Ya sudah, selanjutnya tinggal di commit dan push ke github repository GitPage.

Dan akses dengan url

```
    https://nama.github.io/namaFolderTadi
```

Kalau punya saya ya gini.

```
    https://mashudisudonym.github.io/eatmore
```

Kesimpulan flutter untuk membangun frontend web masih belum stabil dan cukup sulit mengatasi masalah responsif halamannya. Namun, sudah "support" PWA ini adalah kemudahan yang sangat baik.