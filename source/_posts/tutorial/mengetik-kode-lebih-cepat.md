---
title: Mengetik kode lebih cepat
tags:
  - tips
  - web
  - emmet
  - plugin
comments: true
categories: tutorial
date: 2021-10-20 02:55:25
---


{% img /img/tutorial/mengetik-kode-lebih-cepat/banner.jpg '"Person using laptop" "Source: https://unsplash.com/photos/EZSm8xRjnX0"' %}


Bismillahirrahmanirrahim

Disini kita akan belajar tentang, bagaimana mengetik atau menulis kode lebih cepat. Artinya kita tidak perlu mengetikan secara manual, karena ada cara cepatnya. Yang kita bahas dimateri kali adalah mengenai **Emmet**.

{% img /img/tutorial/mengetik-kode-lebih-cepat/logo.svg '"Logo Emmet" "Source: https://emmet.io/"' %}

<!-- more -->


> Jika kalian sudah mengetahu teori dasar tentang emmet, bisa langsung skip ke [Contoh kasus](#Contoh-kasus)

# Teori dasar tentang Emmet

## Apa itu Emmet?

Emmet merupakan sebuah plugin gratis untuk banyak teks editor populer. Khusus untuk Visual Studio Code dan Visual Studio Codium, plugin ini sudah terinstall secara otomatis didalam teks editor tersebut. Selain kedua text editor diatas saya kurang tahu ya, karena dulu saya pernah memakain Sublime Text versi 3. Yang mana emmet nya perlu install secara manual.

Salah satu kegunaan plugin emmet adalah mempercepat alur kerja kita dalam mengetikan perintah HTML dan CSS.

## Apa saja sintaks Emmet?

Saya memberikan beberapa sintaks emmet yang saya ketahui ataupun yang sering digunakan.
### 1. Child (>)
Perintah ini digunakan untuk membuat element bersarang di HTML.

### 2. Sibling (+)
Perintah ini digunakan untuk membuat element setelahnya di tingkatan yang sama.

### 3. Climb-up (^)
Perintah ini digunakan untuk membuat element setelahnya di tingkatan yang berbeda.

### 4. Custom attributes ([])
Perintah ini digunakan ketika ingin menambahkan sebuah element dengan attribute tertentu secara langsung.

### 5. Class attribute (.)
Perintah ini digunakan ketika ingin membuat sebuah element dengan ada nya attribute class di dalam element tersebut.

### 6. Id attribute (#) 
Perintah ini digunakan ketika ingin membuat sebuah element dengan ada nya attribute id di dalam element tersebut.

### 7. Item numbering ($)
Perintah ini digunakan ketika ingin memberikan sebuah angka atau number secara berurut yang dimulai dari 1.

### 8. Text ({})
Perintah ini digunakan ketika ingin memberikan sebuat text didalam element tersebut secara langsung.

### 9. Multiplication (*)
Perintah ini digunakan untuk menduplicate berapa kali element tersebut (sesuai angka yang dimasukkan).

# Contoh kasus

### 1. Child (>)

Contoh penggunaan child, menggunakan tanda **>**.

{% img /img/tutorial/mengetik-kode-lebih-cepat/child.png '"Dengan sintaks child" "Dengan sintaks child"' %}

Untuk membuat sesuai dengan gambar diatas, jika kita menggunakan emmet cukup ketikan `ul>li>a>img`

{% img /img/tutorial/mengetik-kode-lebih-cepat/child.gif '"Gif sintaks child" "Gif sintaks child"' %}

### 2. Sibling (+)

Contoh penggunaan sibling, menggunakan tanda **+**.

{% img /img/tutorial/mengetik-kode-lebih-cepat/sibling.png '"Dengan sintaks sibling" "Dengan sintaks sibling"' %}

Untuk membuat sesuai dengan gambar diatas, jika kita menggunakan emmet cukup ketikan `h1+p+span+p`

{% img /img/tutorial/mengetik-kode-lebih-cepat/sibling.gif '"Gif sintaks sibling" "Gif sintaks sibling"' %}

### 3. Climb-up (^)

Contoh penggunaan climb-up, menggunakan tanda **^**.

{% img /img/tutorial/mengetik-kode-lebih-cepat/climb-up.png '"Dengan sintaks climb-up" "Dengan sintaks climb-up"' %}

Untuk membuat sesuai dengan gambar diatas, jika kita menggunakan emmet cukup ketikan `ul>li>a^img`

{% img /img/tutorial/mengetik-kode-lebih-cepat/climb-up.gif '"Gif sintaks climb-up" "Gif sintaks climb-up"' %}

Disini saya sengaja menggabungkan dengan sintaks child. Jika tidak menggunakan sintaks child, maka tidak akan terlihat perbedaan antara sibling dan climb-up. Karena kedua nya sama yaitu _membuat element setelahnya_, perbedaanya adalah.
- Sibling di tingkatan yang sama
- Climb-up di tingkatan yang berbeda

### 4. Custom Attributes ([])

Contoh penggunaan custom attributes, menggunakan tanda **[]**.

{% img /img/tutorial/mengetik-kode-lebih-cepat/custom-attributes.png '"Dengan sintaks custom-attributes" "Dengan sintaks custom-attributes"' %}

Untuk membuat sesuai dengan gambar diatas, jika kita menggunakan emmet cukup ketikan `button[type="submit" name="btn-submit"]`

{% img /img/tutorial/mengetik-kode-lebih-cepat/custom-attributes.gif '"Gif sintaks custom-attributes" "Gif sintaks custom-attributes"' %}

### 5. Class Attribute (.)

Contoh penggunaan class attribute, menggunakan tanda **.**.

{% img /img/tutorial/mengetik-kode-lebih-cepat/class-attribute.png '"Dengan sintaks class-attribute" "Dengan sintaks class-attribute"' %}

Untuk membuat sesuai dengan gambar diatas, jika kita menggunakan emmet cukup ketikan 
```
.container
p.parapgraph1
a.link_navigation
```

{% img /img/tutorial/mengetik-kode-lebih-cepat/class-attribute.gif '"Gif sintaks class-attribute" "Gif sintaks class-attribute"' %}

### 6. Id Attribute (#)

Contoh penggunaan id attribute, menggunakan tanda **#**.

{% img /img/tutorial/mengetik-kode-lebih-cepat/id-attribute.png '"Dengan sintaks id-attribute" "Dengan sintaks id-attribute"' %}

Untuk membuat sesuai dengan gambar diatas, jika kita menggunakan emmet cukup ketikan 
```
#container
p#parapgraph1
a#link_navigation
```

{% img /img/tutorial/mengetik-kode-lebih-cepat/id-attribute.gif '"Gif sintaks id-attribute" "Gif sintaks id-attribute"' %}

### 7. Item Numbering ($)

Contoh penggunaan item numbering, menggunakan tanda **$**.

{% img /img/tutorial/mengetik-kode-lebih-cepat/item-numbering.png '"Dengan sintaks item-numbering" "Dengan sintaks item-numbering"' %}

Untuk membuat sesuai dengan gambar diatas, jika kita menggunakan emmet cukup ketikan `p.paragraph$`

{% img /img/tutorial/mengetik-kode-lebih-cepat/item-numbering.gif '"Gif sintaks item-numbering" "Gif sintaks item-numbering"' %}

### 8. Text ({})

Contoh penggunaan text, menggunakan tanda **{}**.

{% img /img/tutorial/mengetik-kode-lebih-cepat/text.png '"Dengan sintaks text" "Dengan sintaks text"' %}

Untuk membuat sesuai dengan gambar diatas, jika kita menggunakan emmet cukup ketikan `h1{Ini adalah judul}`

{% img /img/tutorial/mengetik-kode-lebih-cepat/text.gif '"Gif sintaks text" "Gif sintaks text"' %}

### 9. Multiplication (*)

Contoh penggunaan multiplication, menggunakan tanda __*__.

{% img /img/tutorial/mengetik-kode-lebih-cepat/multiplication.png '"Dengan sintaks multiplication" "Dengan sintaks multiplication"' %}

Untuk membuat sesuai dengan gambar diatas, jika kita menggunakan emmet cukup ketikan `p*10`

{% img /img/tutorial/mengetik-kode-lebih-cepat/multiplication.gif '"Gif sintaks multiplication" "Gif sintaks multiplication"' %}

# Menggabungkan seluruh sintaks

{% img /img/tutorial/mengetik-kode-lebih-cepat/combine.png '"Dengan sintaks combine" "Dengan sintaks combine"' %}

Untuk membuat sesuai dengan gambar diatas, jika kita menggunakan emmet cukup ketikan 
```
.container>h1#title+p.paragraph*5{Ini adalah paragraph ke $}^button[type="submit" name="btn-submit"]
```

{% img /img/tutorial/mengetik-kode-lebih-cepat/combine.gif '"Gif sintaks combine" "Gif sintaks combine"' %}

# Emmet untuk CSS?

Jika menggunakan emmet di CSS, itu berguna ketika kalian baru mengetikan `mr`, maka akan disarankan perintah, salah satunya adalah `margin-right`.

Mungkin cukup segini aja yang dapat saya sampaikan, mungkin kedepannya materi ini akan saya **update seiiring dengan menambahnya pengetahuan saya tentang plugin emmet**. Karena pengetahuan saya yang masih sedikit tentang plugin emmet, jadi hanya ini saja yang bisa saya jelaskan di materi ini.

Apabila ada kesalahan mohon dikoreksi di kolom komentar, karena agar kita sama-sama belajar. Apabila ada pertanyaan ataupun masukkan bisa diberikan di kolom komentar atau silahkan chat saya di Telegram [Rian](https://t.me/riann18).

Terima kasih.

Referensi:
- https://emmet.io/
- https://docs.emmet.io/abbreviations/syntax/
- https://kotakode.com/blogs/2782/Mempercepat-Penulisan-HTML-%26-CSS-dengan-Emmet