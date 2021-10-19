---
title: Belajar Git Dasar
tags:
  - Git
  - Web
comments: true
categories: tutorial
date: 2021-10-19 00:01:45
---


{% img /img/tutorial/belajar-git/git.png '"Git logo" "Source: https://git-scm.com/downloads/logos"' %}

Bismillahirrahmanirrahim

Sekarang kita akan membahas mengenai belajar git dasar, saya asumsikan temen-temen sudah menginstall git di sistem operasi masing-masing. Jika belum, silahkan cari di internet cara download dan install git, karena di materi ini saya tidak menjelaskan bagaimana mendownload dan menginstall git.

Disini saya juga masih belajar mengenai git, jadi jika ada kesalahan tolong berikan komentar nya ya, agar saya bisa berkoreksi diri.

Oke, let's go.

<!-- more -->

Sebelum kita praktek mengenai perintah yang ada di git, alangkah baiknya kita sedikit belajar mengenai teori nya, yaitu. Apa itu git.

> Jika sudah mengerti tentang teori dasar git, kamu bisa skip langsung menuju [Perintah Dasar Git](#Perintah-dasar-Git)

# Teori dasar Git

## Apa itu Git?

Jadi, git adalah salah satu dari **Version Control System (VCS)** yang dapat mengetahui _perubahan pada file yang kita kelola_. Tidak hanya untuk mengelola source code saja. Kita juga dapat mengelola file text biasa ataupun mengelola file gambar.

## Apa itu Version Control System (VCS)?

Version Control System sendiri merupakan sistem yang mengelola perubahan pada file. Dengan sistem VCS ini setiap perubahan file akan dipantau dan history perubahannya akan tersimpan. History perubahan yang tersimpan akan menghasilkan string panjang yang unik, itu disebut dengan _hash_ dan untuk menyimpan sebuah perubahan kita harus berikan _commit_.

## Apa itu commit?

Commit adalah pesan yang kita berikan setelah kita melakukan sebuah perubahan pada file kita. Jadi setelah kita selesai melakukan perubahan pada file, setelah kita save. Kita harus commit terlebih dahulu agar git dapat memantau perubahan apa yang telah kita lakukan tadi.

## Apa itu hash?

Hash adalah sebuah string panjang yang unik untuk menandakan setiap kali ada perubahan. Salah satu contoh hash: `c4d0cb8d7c31aee3d686387cbcae4524cda2459d`. 

## Apa manfaat menggunakan Git?

1. Mudah dalam mengelola file
2. Mencegah banyak nya file, jika mengalami banyak perubahan
3. Dapat kembali ke keadaan sebelumnya
4. File tidak terlalu banyak
5. Mudah dalam penggunaannya
6. Dapat berkontribusi pada proyek, khususnya proyek open-source

Banyak sekali bukan kegunaanya? Itu hanya beberapa yang saya tahu dan saya dapatkan di beberapa sumber di internet, mungkin masih banyak lagi manfaat menggunakan git.

Salah satu contoh kasus tanpa menggunakan git.
{% img /img/tutorial/belajar-git/tanpa-git.png '"Tanpa Git" "Tanpa Git"' %}

Setiap perubahan file yang kita lakukan harus membuat file baru / copy paste pada file utama. Mungkin saja untuk membuat backupan file, agar file utama tidak hilang atau jika ingin kembali ke perubahan sebelumnya.

Salah satu contoh kasus menggunakan git.
{% img /img/tutorial/belajar-git/menggunakan-git.png '"Menggunakan-git" "Menggunakan-git"' %}

Setiap perubahan yang kita lakukan akan disimpan oleh Version Control System, dan setiap perubahan kita wajib memberikan commit.

## Apa itu Repo?

Repo adalah singkatan dari Repository, repository adalah sebuah folder yang telah kita **inisialisasi git** pada folder tersebut. Sehingga folder yang telah kita inisialisasi git, itu sekarang kita sebut Repo atau Repository.

## Apa bedanya dengan folder biasa?

Bedanya, folder yang sudah kita inisialisasi git, dapat memantau aktivitas atau perubahan yang kita lakukan pada folder tersebut. Seperti saat kita menambah file, mengubah, atau menghapus. Semua aktivitas itu akan dipantau oleh git.

## Terus apa manfaat nya?

Manfaat nya, kita dapat mengelola project pada folder dengan baik. Dimana saat kita tidak sengaja menghapus file, atau kita bisa juga kembali lagi ke bagian yang kita inginkan.

## The Three States

Pada Git terdapat salah satu bagian penting yang harus kita pahami, yaitu The Three States: modified, staged, dan committed.

### Modified

Modified artinya, jika kita melakukan perubahan seperti: menambah, mengubah atau menghapus file. Tetapi perubahan ini belum disimpan atau dimasukan ke dalam database git lokal secara permanen, database git yang dimaksud adalah folder didalam repo kita yang bernama .git. Folder .git ini default nya adalah hidden atau tidak kelihatan, akan tetapi kita dapat melihatnya dengan melakukan show hidden files di file manager. Folder .git ini tidak perlu kita ubah-ubah, karena akan otomatis diatur oleh git nya sendiri.

### Staged

Staged adalah dimana ketika kita sudah melakukan perubahan pada file, dan ingin menyimpan secara permanen file tersebut di database git lokal atau di repo kita namun belum aman, dimana kita bisa dapat mengubahnya kembali ke status modified. 

### Committed

Committed adalah data atau file kita disimpan dengan aman di database git lokal tersebut, sehingga tidak dapat mengubahnya kembali ke status modified, dan kita bisa mengetahui siapa yang menyimpan data atau file, tanggal disimpan dan juga hash.

## Three Section

Merupakan tempat untuk masing-masing three states sebelumnya, dimana three section ini ada: Working Directory, Staging Area, dan Repository.

### Working Directory

Tempat saat kita melakukan modified, entah itu menambah file, mengubah file, ataupun menghapus file.

### Staging Area

Tempat ketika kita sudah menyimpan secara permanen file dan disimpan di database Git lokal.

### Repository

Setelah file kita sudah berada di staging area, saat nya kita menyimpannya ke repo kita atau ke database git lokal agar aman. Supaya file kita masuk ke dalam Repository yang sebelumnya masih ada di staging area.

# Perintah dasar Git

## git add

Perintah ini digunakan untuk menambahkan file kita kedalam staging area. Kalian bisa menambahkan satu file dengan perintah `git add nama_file`, bisa juga menambahkan lebih dari satu file `git add nama_file1 namaFile2 namaFile3` sesuaikan saja berapa file yang ingin kalian tambahkan. Atau kalian ingin menambahkan sekaligus semua file, gunakan perintah `git add .`. Ya dibelakang nya adalah titik (.).

## git commit

Perintah ini digunakan untuk memberikan pesan terhadap file yang telah kita `git add` sebelumnya, pesan ini bebas mau diisi apa, namun saya sarankan untuk memberikan pesan yang bermakna. Terhadap file yang telah kamu simpan atau kamu `git add`. Perintah untuk commit adalah `git commit -m "Menambahkan pesan hello world"`. Pesan kamu dituliskan didalam kutip, bisa menggunakan kutip satu ataupun kutip dua.

## git log

Perintah ini digunakan untuk melihat daftar semua commit. Perintah nya adalah `git log`.

### git branch

1. Perintah ini digunakan untuk melihat daftar branch, perintah nya adalah `git branch`. 
2. Perintah ini juga bisa membuat sebuah branch, dengan perintah  `git branch nama_branch_baru`.
3. Perintah ini juga bisa menghapus sebuah branch, dengan perintah `git branch -d nama_branch`.

### git checkout

1. Perintah ini digunakan untuk pindah branch ke branch lain, dengan perintah `git checkout nama_branch`.
2. Perintah ini juga bisa digunakan untuk membuat branch baru sekaligus berpindah ke branch yang baru dibuat tersebut, dengan perintah `git checkout -b nama_branch`.

### git clone

Perintah ini digunakan untuk mengambil atau meng-cloning repo yang ada di cloud salah satunya seperti di Github, dapat ada di komputer lokal kita, perintah nya adalah `git clone link_url_repo_github`, contoh nya adalah `git clone https://github.com/mfebriann/CariMobil`. Untuk meng-clone repo [Cari Mobil](https://github.com/mfebriann/CariMobil). 

### git status

Perintah ini digunakan untuk mengecek, apakah file yang telah kita tambahkan sudah di commit atau belum. Ini juga bisa mengecek apakah branch kita tertinggal atau mendahului repo yang telah kita clone. Perintah nya adalah `git status`.

### git remote add

Perintah ini digunakan untuk menambahkan remote ke repo yang telah kita buat di cloud salah satunya seperti Github. Perintah nya adalah `git remote add origin link_url_repo_github.git`. Untuk bagian origin itu bebas saja mau diganti apa, namun umumnya banyak menggunakan origin, dan setelah link url repo itu diberikan .git. Contoh nya adalah `git remote add origin https://github.com/mfebriann/CariMobil.git`.

### git push

Perintah ini digunakan untuk membuat proyek kita yang ada di lokal, dapat ditempatkan di cloud. Perintah nya adalah `git push -u origin nama_branch`. Untuk bagian origin kalian sesuaikan pada saat melakukan remote.

Mungkin cukup segini aja yang dapat saya sampaikan, mungkin kedepannya materi ini akan saya **update seiiring dengan menambahnya pengetahuan saya tentang git**. Karena pengetahuan saya yang masih sedikit tentang git, jadi hanya ini saja yang bisa saya jelaskan di materi ini.

Apabila ada kesalahan mohon dikoreksi di kolom komentar, karena agar kita sama-sama belajar. Apabila ada pertanyaan ataupun masukkan bisa diberikan di kolom komentar atau silahkan chat saya di Telegram [Rian](https://t.me/riann18).

Terima kasih.

Referensi: 
- https://idwebhost.com/blog/pengertian-dan-manfaat-git/
- https://youtu.be/fQbTeNX1mvM
- https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3Fs