---
title: "Digital Fingerprint, Cara Website Identifikasi Pengguna"
date: 2022-11-10 T15:07:43+07:00
draft: false
cover:
  image: "https://images.unsplash.com/photo-1633167606207-d840b5070fc2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=752&q=80"
  alt: "image fingerprint"
---

Apa itu fingerprint ?
=====================

Fingerprint = sidik jari. Sidik jari manusia berbeda setiap orangnya sebagai identitas seseorang. Pada umumnya, pemerintah pasti akan menyimpan data sidik jari seluruh rakyatnya, agar bisa di track/lacak data dan aktifitas setiap individu. Tanpa sidik jari, pemerintah sulit membuat kebijakan.

Apa itu Digital fingerprint ?
=============================

Fingerprint digital seperti sidik jari di dunia nyata. Berfungsi untuk menentukan pengguna yang asli dari beberapa aktifitas. Aktivitas user di internet sulit di track dan dilacak tanpa teknik khusus. Digital fingerprint disini berperan penting dalam tracking user

Kenapa Fingerprint penting untuk website?
=========================================

Ambil contoh sebuah market place yang ingin mengetahui jumlah pengguna pada website mereka. Tapi ada masalah :

1.  Kemungkinan banyak pengguna yang membuat _akun hantu._
2.  Kemungkinan 1 akun digunakan beberapa orang sekaligus
3.  Kemungkinan 1 akun digunakan pada beberapa perangkat sekaligus
4.  Kemungkinan banyak akun spam

Dari masalah-masalah di atas membuat data jumlah pengguna menjadi tidak relevant dan tidak akurat. Jumlah pengguna pada database tidak sama dengan jumlah ‘orang’ yang sebenarnya.

Di sinilah peran digital fingerprint sangat diperlukan. Pemilik website market place perlu membuat sistem untuk mendeteksi user yang membuka websitenya adalah orang yang sama walaupun beda akun dan website dibuka dalam mode incognito (asumsikan bahwa user hanya menggunakan satu browser).

Dengan begitu data fingerprint ini bisa menjadi indikator user yang sebenarnya. Digital fingerprint hanya berupa id dengan format sekumpulan angka dan huruf random yang akan mengeluarkan nilai yang sama ketika user membuka website. Id ini akan di tautkan ke akun user atau disimpan pada server sebagai data digital fingerprint.

Juga berguna jika user mencoba membuat akun sampah pada website, website bisa melabeli user tersebut telah membuat beberapa akun pada satu perangkat.

Bagaimana cara kerja digital fingerprint?
=========================================

Membuat sistem digital fingerprint cukup sulit dan butuh analisa kemungkinan apa yang bisa dilakukan.

Bahasa yang mudah dipahami :  
Fingerprint digital diambil berdasarkan beberapa data yang ada pada browser user, seperti jenis browser, versi browser, tinggi dan lebar layar, jenis device, jenis sistem operasi, dan tipe alat pada komputer/handphone. Semua data ini dikumpulkan dan digabungkan menjadi sebuah id. Data diatas akan menghasilkan id yang berbeda tiap perangkat dan browser.

Bahasa teknikal/programmer :  
Algoritma fingerprint mengambil data-data diatas lalu digabungkan dan di-hash, hasil dari hash adalah id dari user.

Ada beberapa teknik untuk membuat digital fingerprint :

1.  [Tracking pixel.](https://www.cookiepro.com/knowledge/tracking-pixel/) Membuat gambar dengan ukuran 0px dan menggunakan peluang ketika user request gambar ini untuk identifikasi fingerprint.
2.  [Canvas fingerprint](https://en.wikipedia.org/wiki/Canvas_fingerprinting). Website yang memiliki canvas fingerprint akan memaksa browser untuk generate gambar, kemampuan perangkat untuk generate gambar berbeda-beda tiap perangkat. hal ini lah yang diambil untuk dijadikan digital fingerprint.
3.  Browser. Browser sistem memiliki keunikan seperti font yang diinstal, lebar layar, kedalaman warna, spesifikasi browser.
4.  Fingerprint as a service. [Fingerprintjs](https://fingerprintjs.com/). Adalah sebuah service yang memberikan kemudahan website untuk membuat digital fingerprint untuk user.

Apakah ini perlu ditakuti karena melacak user ?
===============================================

Ini hanya alat/tool. Setiap alat tidak punya sifat buruk atau baik, tergantung dari penggunaan alat tersebut yang mendefinisikan baik atau buruk.

Bagi pengusaha, bagi pemilik website hal ini sangat berguna karena mereka dapat insight pengguna merekea dengan baik dan dapat membuat keputusan yang juga untuk pengguna, juga bisa menjadi parameter untuk menyarankan produk untuk pengguna.

Bagi pengguna, hal ini mungkin jadi momok karena pengguna di lacak setiap aktifitas (yang kadang tanpa sadar) dan pemiliki website menggunakan data tersebut untuk menyarankan anda produk yang sesuai untuk anda.

Apakah ini digunakan oleh hacker?
=================================

Well. Ya. Secara teori bisa saja digunakan hacker untuk melacak aktifitas anda. [Hacker akan mengirim link](https://thehackernews.com/2021/10/new-attack-let-attacker-collect-and.html) yang jika dibuka akan mengumpulkan informasi mengenai data browser anda dan menduplikat fingerprint lalu digunakan pada website yang rentan untuk memanipulasi identitas user.

Tapi bukan berarti anda perlu takut, **tips keamanan internet cukup tidak membuka link sembarangan dan tidak memasukkan data pribadi ke website yang tidak dipercaya.**

Apakah saya sudah di-lacak ?
============================

Banyak website yang membuat pelacakan user, google, facebook, tokopedia, gojek, dan lain-lain. Hampir seluruh website besar menggunakan pelacakan ini untuk menyarankan pengguna produk yang cocok.

Buka browser kesukaan anda, lalu akses klik website [coveryourtracks](https://coveryourtracks.eff.org/). Website tersebut akan menganlisa seberapa kuat browser mem-blokir iklan, iklan dan fingerprinting. Browser yang kuat akan muncul seperti ini (saya gunakan [mozilla firefox](https://www.mozilla.org/en-US/))

Jika browser tidak kuat untuk block website akan muncul seperti dibawah ini (saya gunakan microsoft edge)

Saran browser/tool untuk menghindari pelacakan dan iklan
========================================================

Saat ini sudah banyak plugin/add-on browser untuk blokir iklan dan tracker.

1.  [adblockerplus](https://adblockplus.org/) addon browser untuk blokir iklan
2.  [Privacy badger](https://privacybadger.org/) addon browser untuk blokir trakcer
3.  [Brave browser](https://brave.com/) browser yang secara built-in blokir iklan dan tracker

Kesimpulan
==========

Digital fingerprint adalah cara website untuk mengidentifikasi pengguna dan mengatasi masalah spam, robot, dan pengguna yang tidak valid. Digital fingerprint bisa dibuat dengan beberapa teknik dan tidak ada teknik yang dapat akurat 100% karena aktifitas pengguna cukup unik. Ada beberapa plugin dan browser yang dapat mengatasi tracker dan iklan yang kadang menganggu pengguna, karena pengguna juga punya hak terhadap datanya sendiri.

[Dari tulisan saya di medium](https://riochandra.medium.com/digital-fingerprint-cara-website-identifikasi-pengguna-906bea1ef15e)