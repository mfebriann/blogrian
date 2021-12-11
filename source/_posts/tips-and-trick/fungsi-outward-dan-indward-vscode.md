---
title: Fungsi fitur Outward & Inward pada Visual Studio Code
tags:
  - vscode
  - website
  - web
  - html
  - outward
  - inward
  - feature
comments: true
categories: tips&trik
date: 2021-12-10 21:14:46
---


{% img /img/tips-and-trick/outward-&-inward/thumb.jpg '"Thumbnail" "Thumbnail"' %}

Bismillahirrahmanirrahim

Fungsi outward dan inward ini adalah untuk menyeleksi tag pembuka dan penutup dan dapat menyeleksi semua tag didalamnya (child) atau tag diluarnya (parent), jadi kita tidak perlu pusing scroll atau mencari mana tag pembuka atau penutupnya. Mungkin kamu masih sedikit bingung ya mengenai penjelasan ini? Oke untuk lebih jelasnya, saya akan bahas fungsi outward dan inward ini secara detail lagi.

<!-- more -->

## 1. Outward 

Pertama kita akan membahas mengenai fungsi outward. Fungsi outward ini adalah menyeleksi tag pembuka maupun penutupnya, dapat juga menyeleksi element atau tag di dalamnya (child). 

### 1.a) Menyeleksi tag pembuka atau penutup

Contohnya jika meletakan posisi kursor didalam tag pembuka ataupun penutup. Maka dia akan menyeleksi dari tag pembuka dan penutupnya, jika memiliki element atau tag didalamnya maka fungsi outward ini juga akan menyeleksi element atau tag didalamnya. Untuk lebih jelasnya kamu bisa lihat video dibawah ini.

{% img /img/tips-and-trick/outward-&-inward/outward-select-tag.gif '"Seleksi tag pembuka dan tag penutup" "Seleksi tag pembuka dan tag penutup"' %}

Untuk menjalankan outward, terlebih dahulu kita buka command pallete dengan perintah `Ctrl+Shift+P`, lalu kita ketikan `outward`. Seperti yang dijelaskan sebelumnya, jika meletakan cursor didalam tag pembuka ataupun penutup. Maka akan menyeleksi tag pembuka dan penutupnya.

Ini berlaku sama hal nya, jika kamu meletakan posisi kursor diluar tag pembuka. Tetapi _diposisi sebelah kiri_ nya atau jika kamu meletakan posisi kursor diluar tag penutupnya tetapi _diposisi sebelah kanan_ nya.

{% img /img/tips-and-trick/outward-&-inward/outward-outside-tag.png '"Contoh diluar dan disebelah kiri tag pembuka" "Contoh diluar dan disebelah kiri tag pembuka"' %}

### 1.b) Menyeleksi element atau tag didalamnya (child)

Contohnya jika kamu meletakan posisi kursor diluar tag pembuka dan disebelah kanannya, atau kamu bisa juga jika meletakan posisi kursor diluar tag penutup dan disebelah kirinya. Maka jika kita jalankan outward, ia hanya akan menyeleksi element atau tag didalamnya, kita bisa sebut juga child atau anak. Untuk lebih jelasnya kamu bisa lihat video dibawah ini.

{% img /img/tips-and-trick/outward-&-inward/outward-select-child.gif '"Seleksi child pada tag pembuka" "Seleksi child pada tag pembuka"' %}

#### Pertanyaan

1. Lalu bagimana untuk element yang tidak memiliki tag penutup seperti img, input, dan lainnya?

Jawabannya adalah: Jika tidak memiliki tag penutup, jika kita letakan kursor didalam element tersebut lalu kita jalankan perintah outward maka dia akan menyeleksi baris element itu sendiri. Contoh nya bisa lihat video dibawah ini.

{% img /img/tips-and-trick/outward-&-inward/outward-one-line.gif '"Seleksi tanpa tag penutup " "Seleksi tanpa tag penutup "' %}

2. Bagaimana jika kita sengaja atau tidak sengaja menghapus tag penutupnya?

Jawabannya adalah: Jika meletakan kursor didalam tag pembukanya lalu jalankan outward, maka hanya akan menyeleksi tag pembukanya saja. Namun jika meletakan kursor diluar tag pembuka, maka akan menyeleksi seluruhnya sampai berhenti ke parent nya.

{% img /img/tips-and-trick/outward-&-inward/outward-delete-tag.gif '"Seleksi menghapus tag penutup " "Seleksi menghapus tag penutup "' %}

Sedikit penjelasan, ketika tag penutup form dihapus lalu kursor kita letakan diluar tag pembuka, setelah dijalankan perintah outward. Maka dia akan menyeleksi semua nya tapi  **parent nya tidak**. Parent si form adalah **body**, ketika dibuatkan tag main untuk parent si form, maka menyeleksi semuanya kecuali tag main.


## 2. Inward

Hampir sama seperti outward fungsinya, namun bedanya adalah inward hanya untuk menyeleksi child nya saja. Tidak dapat menyeleksi parent nya. Menjalankan perintahnya juga buka command pallete, lalu ketikan `inward`.

#### Perbedaan

1. Jika tidak ada tag penutup, maka tidak dapat di seleksi
{% img /img/tips-and-trick/outward-&-inward/inward-one-line.gif '"Seleksi tanpa tag penutup " "Seleksi tanpa tag penutup "' %}

2. Jika tag penutup tidak ada atau tidak sengaja terhapus, maka akan menyeleksi child pertama nya saja
{% img /img/tips-and-trick/outward-&-inward/inward-delete-tag.gif '"Seleksi menghapus tag penutup " "Seleksi menghapus tag penutup "' %}

3. Jika meletakan posisi kursor didalam tag pembuka atau tag penutup, maka akan menyeleksi semua child nya
{% img /img/tips-and-trick/outward-&-inward/inward-select-child.gif '"Seleksi semua child" "Seleksi semua child"' %}

4. Jika meletakan posisi kursor diluar dan disebelah kanan ataupun kiri tag pembuka atau tag penutup, maka akan menyeleksi child pertama saja
{% img /img/tips-and-trick/outward-&-inward/inward-select-first-child.gif '"Seleksi child pertama" "Seleksi child pertama"' %}

Oke mungkin segitu aja penjelasan saya mengenai outward dan inward yang ada di Visual Studio Code ataupun Visual Studio Codium. Kamu bisa explore lebih jauh lagi mengenai outward dan inward ini.

Oh ya, sedikit tambahan daripada kita ribet atau cape kalo ingin menjalankan outward ataupun inward harus selalu membuka command pallete lalu mengetikan perintahnya. Kita dengan cukup mudah hanya perlu menambahkan keybinding atau shortcut nya.

Caranya kamu buka Keyboard Shortcuts dengan perintah `Ctrl+k` lalu `Ctrl+s`, lalu input pencarian ketikan outward, ketika ketemu arahkan cursor ke pilihan outward lalu klik kanan pada mouse dan pilih **Add Keybinding**. Lalu tentukan shortcut sesuai selera masing-masing lalu enter.
> Catatan: Di cek terlebih dahulu apakah ada keybinding yang sudah dipakai, contoh seperti toggle sidebar yang mana keybinding nya adalah `Ctrl+B`. Jika sudah ada, disarankan untuk tidak menimpa keybinding yang sudah ada.

Bila ada keybinding yang sudah ada, maka akan muncul seperti ini
{% img /img/tips-and-trick/outward-&-inward/error-keybinding.png '"Keybinding sudah ada" "Keybinding sudah ada"' %}

Disini saya berikan keybinding untuk outward yaitu `Ctrl+Alt+b`
{% img /img/tips-and-trick/outward-&-inward/keybinding-outward.gif '"Keybinding outward" "Keybinding outward"' %}

Disini saya berikan keybinding untuk inward yaitu `Ctrl+Alt+v`
{% img /img/tips-and-trick/outward-&-inward/keybinding-inward.gif '"Keybinding inward" "Keybinding inward"' %}

Sekian yang bisa saya bagikan mengenai materi outward dan inward ini, kurang lebihnya mohon dimaafkan. Bila ada kekurangan atau kesalahan jangan sungkan untuk berkomentar untuk memberikan pendapat maupun sarannya, itu sangat saya terima dengan baik. Supaya bisa saya perbaiki.

Jika ingin mengobrol secara pribadi bisa hubungi saya di [Telegram](https://t.me/riann18) atau [Facebook](https://www.facebook.com/mfebrian22/). Semoga catatan ini dapat bermanfaat ya.

Untuk lihat penjelasan secara singkat kamu bisa cek [disini](https://www.instagram.com/p/CXT7F3Ov_eF/?utm_source=ig_web_copy_link).

Sumber referensi:
 - Materi:
   - https://www.youtube.com/watch?v=NwqhFb4B5LU
