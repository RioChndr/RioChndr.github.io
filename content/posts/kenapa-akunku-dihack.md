---
title: "Kenapa Akunku Dihack"
date: 2022-11-10T15:20:51+07:00
draft: false
---

Kenapa akunku bisa dihack ?
===========================

### Problem : Password lemah

Simple : **Akun mu punya password yang lemah.**

Jika anda menyalahkan aplikasi yang digunakan punya cela untuk membuka akun mu, ini kemungkinan ada benarnya kalau aplikasi yang kamu pakai adalah aplikasi dibuat anak Kuliahan yang simpan password di database berupa _plain text_ (dibaca: tidak dikunci). Aplikasi sekarang pada umumnya sudah menggunakan _hash_ untuk menyimpan password pengguna. Hash adalah cara menyimpan identitas password tanpa menyimpan tulisan password itu sendiri. Lengkapnya baca [wikipedia mengenai hash](https://id.wikipedia.org/wiki/Hash).

Aplikasi besar seperti google, youtube, twitter, facebook, netflix, _you name it._ Sudah menggunakan security tingkat tinggi untuk menyimpan data pribadi mu, semuanya disimpan dalam layer-layer yang sangat tebal untuk di jebol. Sangat keciiiil sekali kemungkinan data kamu diambil dari database seperti kasus [tokopedia](https://www.cnbcindonesia.com/tech/20200504094139-37-155966/bahaya-lain-dari-tokopedia-di-hack-91-juta-data-bocor).

Tapi, walaupun di hack dan diambil data kamu dari database seperti tokopedia. PASSWORD KAMU TETAP AMAN !!. Itulah kekuatan dari [Hashing](https://id.wikipedia.org/wiki/Hash). Walaupun hacker ambil password kamu dari database, mereka harus memakan waktu yang cukup lama untuk menemukan password kamu yang sebenarnya. TAPI !, kalau password kamu lemah seperti “rio123”, “12345678”, “password123”. Cukup hitungan menit untuk hack akun kamu !

Lihat table berikut

![Time to crack password](/image/time-to-crack-passwd.jpeg)

Solusi : Forget password
========================

Kalau akun mu di hack, gunakan fitur _forget password_ pada aplikasi yang kamu gunakan. Cara ini cukup mudah jika kamu bisa akses email mu

![Forget password](https://miro.medium.com/max/720/1*Sd_XFcyYBhkhBf6js9HwdQ.png)

![Reset password](https://miro.medium.com/max/720/1*qsqFLuY8587oNdR59F694A.png)

Aplikasi akan mengirimkan kode ke email mu untuk verifikasi. Masukkan kode tersebut ke kolom yang tersedia. Maka kamu bisa ubah password akun mu.

![security code](https://miro.medium.com/max/720/1*-zzUU50PFuF_9atNKUYVng.png)

![security code fb](https://miro.medium.com/max/640/1*HbwZIoD3UHpButNi88KM4w.png)

Cara ini cukup mudah dan efektif. Tapi jika kamu tidak memiliki akses ke email, maka **Ikhlaskan akun tersebut !**

Tingkatkan keamanan akun kamu !
===============================

Aplikasi sudah menyimpan dan mengaman kan akun mu, sekarang kamu yang ambil peran untuk mengamankan akun mu. Buat password yang aman :

*   Jangan gunakan nama kamu, tanggal lahir, angka yang mudah di tebak : contoh : budi123, budi123456, 1234budi, 12345678, bud1412.
*   Jangan Gunakan password yang sama pada semua akun ! (kesalahan paling umum), password sudah kuat tapi digunakan pada semua akun.
*   Password harus memiliki karakter huruf, angka dan karater unik.
*   Minimal panjang 8 karakter, maksimal ? terserah kamu, makin panjang makin bagus

Lupakan password, simpan di password manager
============================================

> **Jangan ingat password kamu, buat se-random mungkin. Simpan di aplikasi password manager.**

Di internet sudah banyak aplikasi password manager gratis, bebas mau simpan berapa juta password didalamnya, mereka sudah mengikuti standarisasi kemanan pada umumnya.

Problem password manager : _Ribet harus buka password manager kalau login lagi_

Malah ini lebih bagus, **karena kamu punya kesadaran untuk login ke device baru dan tidak sembarangan login.**

Contoh password manager gratis yang bisa kamu gunakan

*   [Bitwarden](https://bitwarden.com/). Open source, gratis
*   [Dashlane](https://www.dashlane.com/). Gratis, Ui bagus
*   [Lastpass](https://www.lastpass.com/). Gratis, Modern
*   [1Password](https://1password.com). Gratis, Ui bagus