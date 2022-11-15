---
title: "Designer ke Developer Handoff"
date: 2022-11-15T21:27:41+07:00
draft: true
cover:
  image: ""
  alt: ""
  relative: false # To use relative path for cover image, used in hugo Page-bundles
---

# Panduan Handoff Designer ke Developer

Saat ini Desain aplikasi tidak pernah semudah ini dari pada sebelumnya. Sudah banyak aplikasi seperti [Figma](https://figma.com) atau [adobe xd](https://adobe.com) yang memiliki fitur *Realtime collaboration*, ini memudahkan developer yang tidak perlu menunggu desain selesai sepenuhnya dan bisa langsung kolaborasi secara *realtime*.

*Handoff* artinya **Serah Terima**, proses pengiriman desain ke developer untuk dieksekusi. Banyak kesalahan fatal dari Designer UI/UX saat mengirimkan desainnya kepada developer yaitu **hanya mengirimkan**. Bagi stakeholder atau project owner pasti mudah terima karena cukup melihat hasil akhir, tapi bagi developer yang cara berpikirnya "Jika ini maka ini." dan cukup detail. Tak jarang developer yang pertama kali melihat desain UI terkaget lalu berkata "APA ? Kalau begini gimana ?, Ini tombolnya kemana? ini aksinya gimana ?". Bertanya dan menjelaskan langsung pada saat itu sangat membuang waktu dan jangan percaya ingatan manusia yang mudah lupa.

Metode handoff ini harapannya bisa membantu desainer dan developer berkomunikasi dengan baik tanpa developer atau team lead bertanya-tanya banyak hal yang tidak perlu lagi.

Ini bukanlah metode standard industri, tapi inti dari pemabahasan ini adalah bagaimana management desain untuk dikirimkan kepada developer tanpa membuang waktu untuk menjelaskan satu-persatu. Semua yang ada disini hanya berdasarkan referensi saya pribadi dan beberapa riset mengenai metode handoff desain.

## Management File

Mengingat desainer sangat berinteraksi dengan file dan folder, pastikan file memiliki format yang rapi dan terurut, tidak dicampur-adukkan semua desain. Pada umumnya desain UI terbagi beberapa yaitu **Low-fi**, **Wireframe**, dan **High-fi**.

```
Folder desain 
- wireframe
- lo-fi
- mockup
- hi-fi

* Bisa ditambah atau dikurangi berdasarkan kebutuhan
```

Saat ini, pengembangan aplikasi sudah menggunakan iterasi (atau sprint). File Desain perlu dipisahkan agar dapat track perubahan setiap iterasi. Lebih baik jika sub folder berisi jenis desain.

```
Folder desain
- iterasi 1
  - lo-fi
  - hi-fi
- iterasi 2
  - lo-fi
  - hi-fi
```

Management file ini sangat berguna selain untuk developer, juga berguna untuk desainer selanjutnya yang akan memegang projek yang sama. Jika bisa didokumentasikan dengan baik itu lebih bagus.

## Design System

Sistem Desain (Design System) adalah seperangkat pola yang saling berhubungan dan praktik bersama yang diatur secara koheren [^wikipedia](https://en.wikipedia.org/wiki/Design_system#cite_note-1). Design system membuat pola dari aplikasi yang dibuat, bagaimana bentuk tombol ? bentuk form ? size ? space margin/padding ? warna ? error ? warning ? text ?. Design System menjawab semua ini. Ini sangat membantu developer dan membantu desainer untuk tetap konsisten pada setiap halaman.

## Dokumentasi dan anotasi

Dokumentasi desain perlu dibuat, desainer tidak perlu menjelaskan satu-persatu saat meeting, cukup beri gambaran besar dan sisanya akan dijelaskan dari dokumenasi. Step ini **Tidak boleh** dilewatkan saat ingin handoff kepada developer.

Saat ini aplikas desain UI sudah sangat membantu untuk dokumentasi teknis seperti size, space margin/padding, ukuran text, hingga kode warna sudah menjadi fitur utama aplikasi desain. Tapi dokumentasi flow dan aplikasi perlu dibuat manual, dokumentasi harus berupa : 

- *Flow*, dari page mana ke mana ?
- *Behaviour*, Bagaimana perilaku user terhadap desain ?
- *Requirement*, Apa saja spesifikasi desainnya ?
- *API*, API yang digunakan ?

Selain poin-poin diatas, dokumentasi Desain bisa melingkupi seperti kondisi *if else*. Semakin lengkap dokumentasi desain, semakin cepat pengerjaan developer, tidak perlu menghabiskan waktu untuk menjelaskan berulang-ulang.

## *Think Like Developer*

Developer selalu berpikir menggunakan logika. Berpikir logis, detail dan teratur adalah kebiasaan developer.

> Semua orang bisa membuat desain, tapi desainger yang baik adalah Desain yang logis, detail dan teratur.

Desain yang logis maksudnya adalah desain yang memiliki flow yang masuk akal dan sesuai dengan kebutuhan bisnis. Desain yang detail menjelaskan bagaimana behaviour user terhadap tampilan UI, bisa jadi ada beberapa cabang flow, flow yang detail dapat menggambarkan kondisi yang sebenarnya. Teratur adalah bagaimana menjelaskan melalui desain konsep gambaran kasar (lo-fi) ke gambaran detail (high-fi)

## Beri Opsi

Developer terkadang memiliki pertimbangan apakah desain tersebut dapat dikerjakan dalam waktu singkat atau tidak. Beri kebebasan kepada developer untuk memilih yang mana paling possible dijalankan.

Memberikan opsi 1-2 halaman dengan fitur yang sama dapat memudahkan developer dan tim lainnya untuk memilih agar tidak perlu lagi revisi tampilan. *Manusia menyukai pilihan, karena dia merasa memiliki kuasa dan punya kontrol.*

## Tools Referensi


## Kesimpulan