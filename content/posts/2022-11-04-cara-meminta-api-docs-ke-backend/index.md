---
title: "Cara Meminta Api Docs ke Developer Backend dari Developer Frontend"
date: 2022-11-10T23:08:15+07:00
draft: false
tags: ['Development', 'Blogging', 'Tips']
cover:
  image: "arisa-chattasa-0LaBRkmH4fM-unsplash.jpg"
  alt: "arisa-chattasa-0LaBRkmH4fM-unsplash.jpg unsplash"
  relative: true # To use relative path for cover image, used in hugo Page-bundles
---

## Pendahuluan

Bagi projek yang tidak memiliki [**Product Requirement Document (PRD)**](https://www.atlassian.com/agile/product-management/requirements), sangat sulit untuk menganalisa aplikasi dan requirement hanya dari beberapa kali meeting, ini saya alami sendiri dari projek freelance yang tidak memiliki PRD, dokumen pendukung dan hanya diberikan desain yang minim info. Penjelasan detail hanya dijelaskan dari meeting yang terbatas ruang dan waktu.

Bagi frontend sangat membutuhkan informasi seperti lokasi API, payload, flow desain, data, validasi data, hingga *error handling*. Tanpa dokumen yang baik, akan menjadi *diseaster* bagi projek kedepannya, sangat mudah terjadi miss-komunikasi, *bugs*, hingga projek yang tidak di maintain dengan baik.

Ada baiknya, dokumen seperti PRD (minimal) tersedia untuk frontend, backend, desainner, hingga projek owner. Dokumen seperti ini menjadi bahan diskusi dan sumber komunikasi antar tim. Tapi projek freelance sangat terbatas dengan waktu dan tim yang mumpuni, maka saya akan jelaskan format data yang bisa digunkan untuk meminta tim backend menjelaskan API tanpa meeting berkali-kali.

## Tentukan Lokasi Dokumen

Tulis kebutuhan di sebuah tempat online yang bisa di *share* secara online. Usahakan tempat menulis support markdown (Jika kamu prefer markdown), bisa menggunakan [Github issue](https://github.com/features/issues), [Trello](https://trello.com), [Jira](https://www.atlassian.com/software/jira). atau bisa menggunakan [Google docs](https://docs.google.com)

## Penulisan dokumen

Tidak ada format khusus untuk menulis dokumen API. Semuanya tergantung kebutuhan masing-masing. Tapi saya berikan gambaran kasar mengenai format dokumen API

```markdown
## Judul Fitur

> Kepada tim backend, mohon update bagian ini.

### Action Create

API : `POST /post`
Payload
` ` `
{
  title: 'string',
  description: 'string'
}
` ` `

Link Design \& flow : Mohon isi link desain (figma, adobe xd)

Conditional : 
- jika title lebih dari 50 karakter, ada pesan error

Question for backend : 
- Tolong tulis property mana yang punya validasi form (eg: required)
- jika ada tambahan property payload, mohon di update
- Apakah API ini hanya bisa diakses oleh admin ?
- Setelah menyimpan dokumen apakah pindah ke page list atau detail post ?
```

Ada beberapa point yang perlu ditulis dalam dokumen ini :

1. **Judul**, ini bisa berupa nama fitur atau flow
2. **Action**, karena biasanya REST API dibuat berdasarkan action yang dilakukan, maka tulis actionnya.
3. **Path REST API**, jika tidak tahu, tulis saja `API : need verification`.
4. **Payload**, data API sebagai konfirmasi ke backend walaupun di swagger sudah lengkap. kalau bisa ini dicantumkan example payload.
5. **Question**, pertanyaan-pertanyaan ini berguna untuk menjawab pertanyaan simple tapi memiliki dampak yang besar. Tanpa lakukan meeting yang lama, cukup tulis pertanyaan disini.

## Kirim ke Tim Developer Backend

Kirim dokumen tersebut ke tim backend, kalau bisa mereka memiliki akses ke dokumen untuk langsung di update dan melakukan diskusi secara online. Perlu adanya konfirmasi ke tim backend dan monitor setiap 1x24 jam memastikan tim backend mengingat tugas melengkapi dokumen ini.

## Jangan takut

Meminta kejelasan bukan sebuah kesalahan, lebih baik lakukan ini dari pada projek menjadi ribet nantinya, tidak terorganisir dan menjadi hilang arah kedepannya. Inisiatif dari kita dibutuhkan untuk menjadikan projek berjalan dengan baik.

## Kesimpulan

Dokumen requirement sangat diperlukan dalam sebuah projek sebagai sumber informasi (*single source of truth*) yang dapat digunakan oleh semua bagian tim baik dari management, project owner, developer, designer. Walaupun contoh yang saya berikan bukan sebuah contoh yang memiliki standard, tapi point utama dari pembahasan ini adalah bagaimana membagikan informasi antar tim tanpa terjadi miss-komunikasi yang biasa terjadi.