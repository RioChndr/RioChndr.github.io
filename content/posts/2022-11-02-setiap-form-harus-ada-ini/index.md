---
title: "Setiap Form Harus Ada Ini"
date: 2022-11-10T15:32:23+07:00
draft: false
tags: ['Development', 'Info', 'Tips']
cover:
    image: "https://images.unsplash.com/photo-1543966888-7c1dc482a810?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1506&q=80"
    alt: "Setiap form harus ada ini"
    relative: true # To use relative path for cover image, used in hugo Page-bundles
---

Setiap website yang memiliki data CRUD pasti memiliki form. Setiap form juga harus memiliki beberapa fitur berikut :

1. Form Field
  Form field adalah komponen data-data yang akan disimpan. Form harus jelas, ada label, deskripsi sebagai opsional, contoh data dan placeholder.
2. Validation
  Validasi data penting untuk memastikan yang di input user sesuai dengan apa yang seharusnya.
3. Action
  Action bisa berupa tombol ‘simpan’, ‘cancel’. Tombol ini harus jelas dan terlihat. Tombol simpan biasanya memiliki tombol dengan background berwarna dan tombol cancel memiliki style outlined.
4. Loading
  Setelah user klik tobol action, harus memiliki loading. Loading sebagai tanda bahwa ada hal yang sedang terjadi. Indikator dari loading ini bisa banyak jenis.
5. File (Jika ada)
  Jika file berupa gambar atau video, tampilkan preview file. Selain kedua tipe tersebut hanya tampilkan nama file, opsional tampilkan ukuran file. Khusus file, perlu beri indikator progress upload.
6.  Response
  Response berhasil simpan perlu di tampilkan dan response gagal juga perlu ditampilkan. pastikan response ini tidak mengganggu user. Jangan gunakan alert dialog atau popup dialog karena ini sangat mengganggu

Sebagai catatan, semua point diatas adalah hasil best practice secara personal terhadap pekerjaan yang pernah dikerjakan.