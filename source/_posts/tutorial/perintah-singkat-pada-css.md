---
title: Perintah singkat pada CSS (Shorthand)
tags:
  - css
  - layout
  - website
comments: true
category: tutorial
date: 2021-12-02 09:02:40
---


{% img /img/tutorial/perintah-singkat-pada-css/thumbnail.jpg '"Thumbnail"  "Thumbnail"' %}

Bismillahirrahmanirrahim

Kali ini saya akan membahas mengenai tulisan cepat atau shorthand pada perintah css, yang mana ini akan membantu menghemat waktu pekerjaan kita dalam membuat sebuah website. Khusus nya pada bagian css.

Diharapkan kalian sudah mengetahui apa itu css, ekstensi pada file css dan beberapa perintah nya, begitu juga dengan html agar sepaket hehe. Jika belum, saya sarankan untuk pelajari terlebih dahulu mengenai kedua hal tersebut. 

<!-- more -->

Mungkin dari kita masih ada yang menggunakan cara lambat dalam perintah css, walaupun tidak dipermasalahkan juga. Namun alangkah lebih baik jika kita mencoba beberapa shorthand pada perintah css agar dapat menghemat waktu. Banyak sekali shorthand pada perintah css, seperti **margin**, **padding**, **border**, dan masih banyak lagi. 

## 1. Margin
{% img /img/tutorial/perintah-singkat-pada-css/margin-4-value.png '"Margin dengan 4 nilai"  "Margin dengan 4 nilai"' %}

Pada perintah diatas terdapat 4 nilai, yang dimana cara membaca nya seperti jarum jam. Dari atas, kanan, bawah, dan kiri.

Jadi nilai pertama 20px itu menandakan **bagian atas** margin, lalu 30px menandakan **bagian kanan** margin, lalu 10px menandakan **bagian bawah** margin dan 20px nilai terakhir itu menandakan **bagian kiri** margin. Jadi penulisannya lebih singkat. 

Daripada kita harus mengetikan perintah margin satu persatu, seperti `margin-top` ketika ingin menandakan bagian atas, `margin-bottom` ketika ingin menandakan bagian bawah, dan seterusnya.

- ### 1.A) Margin 3 nilai
{% img /img/tutorial/perintah-singkat-pada-css/margin-3-value.png '"Margin dengan 3 nilai"  "Margin dengan 3 nilai"' %}

Apa maksudnya margin dengan 3 nilai seperti gambar diatas?

Kalo 3 nilai seperti itu cara baca nya adalah, nilai pertama untuk margin **bagian atas** 20px, nilai kedua untuk margin **bagian kiri dan kanan** 30px dan nilai terakhir untuk margin **bagian bawah** 10px. Cara baca nya tetap seperti jarum jam, seperti yang dijelaskan sebelumnya.

- ### 1.B) Margin 2 nilai
{% img /img/tutorial/perintah-singkat-pada-css/margin-2-value.png '"Margin dengan 2 nilai"  "Margin dengan 2 nilai"' %}

Apa maksudnya margin dengan 2 nilai seperti gambar diatas?

Kalo 2 nilai seperti itu cara baca nya adalah, nilai pertama untuk margin **bagian atas dan bawah** 20px dan nilai kedua untuk margin **bagian kiri dan kanan** 30px.

- ### 1.C) Margin 1 nilai
{% img /img/tutorial/perintah-singkat-pada-css/margin-1-value.png '"Margin dengan 1 nilai"  "Margin dengan 1 nilai"' %}

Apa maksudnya margin dengan 1 nilai seperti gambar diatas?

Kalo 1 nilai seperti itu cara baca nya adalah, untuk **semua bagian** pada margin yaitu atas, kanan, bawah dan kiri nilai nya 20px.

## 2. Padding
{% img /img/tutorial/perintah-singkat-pada-css/padding-4-value.png '"Padding dengan 4 nilai"  "Padding dengan 4 nilai"' %}

Perintah pada padding sama persis seperti margin, hanya saja perintah nya yang beda yaitu menggunakan `padding`.

## 3. Border
{% img /img/tutorial/perintah-singkat-pada-css/border.png '"Shorthand border"  "Shorthand border"' %}

Untuk shorthand pada border dibutuhkan 3 nilai saja, yaitu nilai pertama untuk tebal / lebar border, nilai kedua style pada border dan nilai ketiga warna pada border. Jadi kita cukup mengetikan satu perintah saja yaitu `border`. Tanpa perlu `border-width`, `border-style`, dan `border-color`. Yang mana cukup panjang.

## 4. Border-radius
{% img /img/tutorial/perintah-singkat-pada-css/border-radius.png '"Shorthand border-radius 4 nilai"  "Shorthand border-radius 4 nilai"' %}

Untuk shorthand pada border-radius yang kita coba dengan 4 nilai terlebih dahulu, terus apa maksudnya?

Maksudnya adalah, nilai pertama itu untuk **bagian atas kiri**, nilai kedua untuk **bagian atas kanan**, nilai ketiga untuk **bagian bawah kanan** dan nilai terakhir untuk **bagian bawah kiri**. Tanpa perlu kita ketikan perintah nya satu persatu, seperti `border-top-left-radius`, `border-top-right-radius`, dan seterusnya.

- ### 4.A) Border-radius 3 nilai
{% img /img/tutorial/perintah-singkat-pada-css/border-radius-3-value.png '"Shorthand border-radius 3 nilai"  "Shorthand border-radius 3 nilai"' %}

Shorthand border-radius dengan 3 nilai cara bacanya, nilai pertama itu untuk **bagian atas kiri**, nilai kedua untuk **bagian atas kanan dan bagian bawah kiri** dan nilai ketiga untuk **bagian bawah kanan**.

- ### 4.B) Border-radius 2 nilai
{% img /img/tutorial/perintah-singkat-pada-css/border-radius-2-value.png '"Shorthand border-radius 2 nilai"  "Shorthand border-radius 2 nilai"' %}

Shorthand border-radius dengan 2 nilai cara bacanya, nilai pertama itu untuk **bagian atas kiri dan bagian bawah kanan** dan nilai kedua untuk **bagian atas kanan dan bagian bawah kiri**.

- ### 4.C) Border-radius 1 nilai
{% img /img/tutorial/perintah-singkat-pada-css/border-radius-1-value.png '"Shorthand border-radius 1 nilai"  "Shorthand border-radius 1 nilai"' %}

Shorthand border-radius dengan 1 nilai cara bacanya, nilai pertama itu untuk **semua bagian**.

## 5. Background
{% img /img/tutorial/perintah-singkat-pada-css/background.png '"Shorthand background"  "Shorthand background"' %}

Jika kita ingin menggabungkan antara background color dengan background image, agar lebih ringkas coba gunakan shorthand sesuai gambar diatas.

## 6. Top, Bottom, Left, Right
{% img /img/tutorial/perintah-singkat-pada-css/inset.png '"Shorthand inset"  "Shorthand inset"' %}

Jika nilai left, bottom, left, dan right nilai nya sama. Kita bisa lebih ringkas gunakan perintah `inset`.

## 7. Transition
{% img /img/tutorial/perintah-singkat-pada-css/transition.png '"Shorthand transition"  "Shorthand transition"' %}

Cara baca nya adalah, nilai pertama merupakan **durasi waktu transisi** nya, nilai kedua **timing function** dan yang terakhir **delay transisi**.

## 8. Animation
{% img /img/tutorial/perintah-singkat-pada-css/animation.png '"Shorthand animation"  "Shorthand animation"' %}

Sama seperti transition, namun urutan petama nya merupakan **nama animasi** yang dibuat dari `@keyframes`.

## 9. Grid column
{% img /img/tutorial/perintah-singkat-pada-css/grid-column.png '"Shorthand grid-column"  "Shorthand grid-column"' %}

Shorthand untuk grid, dimana menjelaskan tentang ukuran dan lokasi column.

## 10. Grid row
{% img /img/tutorial/perintah-singkat-pada-css/grid-row.png '"Shorthand grid-row"  "Shorthand grid-row"' %}

Shorthand untuk grid, dimana menjelaskan tentang ukuran dan lokasi row.

## 11. Gap
{% img /img/tutorial/perintah-singkat-pada-css/gap.png '"Shorthand gap"  "Shorthand gap"' %}

Shorthand untuk grid, dimana menjelaskan tentang memberikan celah / jarak pada column atau row. Ketika kita berikan dua nilai, itu artinya nilai pertama itu untuk **memberikan celah pada row** dan nilai kedua **memberikan celah pada column**. Namun jika hanya yang diberikan hanya satu nilai. Maka **memberikan celah pada row dan column**.

Sekian, shorthand atau penulisan cepat pada perintah di css yang mana bisa membantu kalian, salah satunya membantu dalam menghemat waktu. Dengan shorthand ini, kita tidak perlu mengetikan banyak perintah. Itu beberapa shorthand yang dapat saya bagikan, karena ada beberapa yang saya sering gunakan. 

Apabila ada komentar berupa kritik dan saran terhadap catatan ini. Jangan ragu untuk berkomentar ya :). Sampai jumpa dipertemuan berikutnya, semoga bermanfaat.

Sumber referensi: 
- https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties