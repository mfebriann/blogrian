---
title: Revisi Form Pemesanan Tiket
tags:
  - html
  - css
  - js
  - form
  - tiket
comments: true
categories: tutorial
date: 2022-07-25 13:00:56
---


{% img /img/tutorial/revisi-program-pemesanan-tiket/1.png '"Tampilan Program" "Tampilan Program"' %}

Halo semuanya, sudah lama sekali saya tidak aktif lagi menulis di blog ini dikarenakan ada beberapa urusan yang harus dikerjakan terlebih dahulu. Oke kita langsung ke pembahasan intinya, jadi disini saya akan membagikan tutorial revisi dari form pemesanan tiket yang sebelumnya pernah kita bahas.

Jika kamu belum melihat form pemesanan tiket yang awal, kamu bisa lihat nya [Membuat Form Pemesanan Tiket](https://blogrian.my.id/tutorial/membuat-form-pemesanan-tiket/). Bagi yang belum lihat bisa di cek dulu ya, oke langsung kita revisi form nya. Let's go.

<!-- more -->

Jadi untuk demo dari revisi website form pemesanan tiket kita akan menjadi seperti ini.
{% img /img/tutorial/revisi-program-pemesanan-tiket/demo.gif '"Demo Program" "Demo Program"' %}

Keren bukan? Untuk membuat tampilan seperti itu kita harus merubah (Jika kalian sudah membuat form pemesanan tiket sebelumnya) atau membuat file html, lalu tuliskan kode berikut.
{% codeblock index.html lang:html %}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ticket Payment</title>
    <!-- Icon -->
    <link rel="shortcut icon" href="plane-landing.png" type="image/x-icon" />
    <!-- Font -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600&display=swap" rel="stylesheet" />
    <!-- Lokasi file CSS -->
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <main>
      <section class="container">
        <!-- Bagian form input  -->
        <div class="item-content item-content--form">
          <div class="content">
            <h2 class="title-form">Isi formulir untuk pembelian tiket</h2>
            <form>
              <div class="wrap-input">
                <label for="name">Nama:</label>
                <input type="text" id="name" autofocus autocomplete="off" class="input-form" required />
              </div>

              <div class="wrap-input">
                <label for="city">Kota Dituju:</label>
                <input type="text" id="city" list="list-city" autocomplete="off" class="input-form" required />

                <!-- Daftar kota tujuan -->
                <datalist id="list-city">
                  <option value="Malang">Malang</option>
                  <option value="Magelang" data-discount="5">Magelang</option>
                  <option value="Medan">Medan</option>
                  <option value="Yogyakarta">Yogyakarta</option>
                  <option value="Lampung">Lampung</option>
                  <option value="Pekanbaru">Pekanbaru</option>
                  <option value="Palembang" data-discount="10">Palembang</option>
                  <option value="Makassar">Makassar</option>
                  <option value="Papua" data-discount="5">Papua</option>
                  <option value="Ambon" data-discount="15">Ambon</option>
                  <option value="Balikpapan">Balikpapan</option>
                  <option value="Pontianak">Pontianak</option>
                  <option value="Bandung" data-discount="10">Bandung</option>
                  <option value="Jakarta" data-discount="10">Jakarta</option>
                  <option value="Surabaya">Surabaya</option>
                </datalist>
              </div>

              <div class="wrap-input">
                <label for="status">Status:</label>
                <select name="statu" id="status" class="input-form" required>
                  <option value="Dewasa">Dewasa</option>
                  <option value="Anak-anak">Anak-anak</option>
                </select>
              </div>

              <div class="wrap-input">
                <label for="total-people">Jumlah Orang:</label>
                <input type="number" id="total-people" class="input-form" required />
              </div>

              <div class="wrap-input">
                <label for="payment-method">Metode Pembayaran:</label>
                <!-- Daftar pembayaran -->
                <select name="payment" id="payment-method" class="input-form" required>
                  <option value="BRI">BRI</option>
                  <option value="BCA">BCA</option>
                  <option value="BNI">BNI</option>
                  <option value="Mandiri">Mandiri</option>
                  <option value="DANA">DANA</option>
                  <option value="OVO">OVO</option>
                  <option value="Gopay">Gopay</option>
                </select>
              </div>

              <div class="wrap-input">
                <label for="discount">Diskon:</label>
                <input type="text" id="discount" class="input-form input-form--disabled" disabled value="0%" required />
              </div>

              <div class="wrap-btn">
                <button type="reset" class="btn btn--reset">Hapus</button>
                <button type="submit" class="btn btn--send">Pesan</button>
              </div>
            </form>
          </div>

          <img src="https://images.unsplash.com/photo-1473116763249-2faaef81ccda?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=896&q=80" alt="vacation" class="img-container" />
        </div>

        <!-- Bagian output -->
        <div class="item-content item-content--output-payment">
          <div class="content">
            <h2 class="title-form">Konfirmasi detail pembelian tiket</h2>
            <div class="confirmation-detail">
              <div class="container-description-output">
                <p class="description-output">Nama:</p>
                <p class="value-output">Joko</p>
              </div>
              <div class="container-description-output">
                <p class="description-output">Kota Dituju:</p>
                <p class="value-output city">Jakarta</p>
              </div>
              <div class="container-description-output">
                <p class="description-output">Status:</p>
                <p class="value-output">Dewasa</p>
              </div>
              <div class="container-description-output">
                <p class="description-output">Jumlah Orang:</p>
                <p class="value-output">4</p>
              </div>
              <div class="container-description-output">
                <p class="description-output">Harga 1 tiket:</p>
                <p class="value-output">Rp.150.000</p>
              </div>
              <div class="container-description-output">
                <p class="description-output">Subtotal Pembayaran:</p>
                <p class="value-output">Rp.600.000</p>
              </div>
              <div class="container-description-output">
                <p class="description-output">Diskon:</p>
                <p class="value-output">10%</p>
              </div>
              <div class="container-description-output">
                <p class="description-output">Total Pembayaran:</p>
                <p class="value-output">Rp.540.000</p>
              </div>
              <div class="container-description-output">
                <p class="description-output">Metode Pembayaran:</p>
                <p class="value-output">BRI</p>
              </div>
            </div>
            <div class="wrap-btn wrap-btn--confirmation-detail">
              <button type="button" class="btn btn--edit">Ubah</button>
              <button type="button" class="btn btn--pay" id="btn-pay">Bayar</button>
            </div>
          </div>

          <img src="https://images.unsplash.com/photo-1593182440959-9d5165b29b59?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=871&q=80" alt="vacation" class="img-container" />
        </div>

        <!-- Pembelian tiket berhasil -->
        <div class="item-content item-content--payment-success">
          <div class="content">
            <div>
              <h2 class="title-form">Pembayaran tiket berhasil, selamat menikmati liburan.</h2>
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="64" height="64" class="icon-success-payment">
                <path fill="none" d="M0 0h24v24H0z" />
                <path d="M10 15.172l9.192-9.193 1.415 1.414L10 18l-6.364-6.364 1.414-1.414z" fill="rgba(46,207,115,1)" />
              </svg>
              <p class="detail-data-payment">Lihat detail data pembelian tiket</p>
            </div>
          </div>

          <img src="https://images.unsplash.com/photo-1507539989371-99615e449486?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=962&q=80" alt="happy-vacation" class="img-container" />
        </div>
      </section>

      <div class="popup-confirmation popup">
        <div class="subpopup-confirmation subpopup">
          <p class="description-popup-confirmation">Apakah data pembelian tiket sudah benar?</p>
          <div class="wrap-btn">
            <button class="btn btn--no" type="button">Belum</button>
            <button class="btn btn--yes" type="button">Sudah</button>
          </div>
        </div>
      </div>

      <div class="popup-check-detail-data popup">
        <div class="check-detail-data subpopup">
          <!-- Isi konten detail data ini dinamis dari javascript -->
        </div>
      </div>
    </main>
  <!-- Lokasi file javascript -->
  <script src="script.js"></script>
  </body>
</html>
{% endcodeblock %}

Dari kode diatas nanti akan menghasilkan tampilan seperti ini.
{% img /img/tutorial/revisi-program-pemesanan-tiket/html.png '"Tampilan awal HTML" "Tampilan awal HTML"' %}

Baris 9 pada kode diatas, itu merupakan icon yang bisa kamu sesuaikan dengan icon di folder project kamu ya dan abaikan saja untuk tampilannya yang masih kurang menarik, dikarenakan kita belum menambahkan CSS nya. 

Agar tampilan terlihat lebih cantik dan menarik, kita bisa menambahkan CSS. Dan kamu bisa tuliskan kode css nya seperti ini.
{% codeblock style.css lang:css %}
* {
  box-sizing: border-box;
}

/* Men-disabled spinners pada input number */
/* Chrome, Safari, Edge, Opera */
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

/* Firefox */
input[type='number'] {
  -moz-appearance: textfield;
}

body,
input,
button {
  font-family: 'Poppins', sans-serif;
}

body {
  margin: 0;
  height: 100vh;
}

h2,
p {
  margin: 0;
}

main {
  transition: background-color 500ms ease-in-out;
  background-color: #566f83;
  padding: 10px;
  width: 100%;
  height: 100%;
  display: grid;
  place-items: center;
}

main.active {
  background-color: #7bb077;
}

.container {
  width: 1024px;
  margin: 0 auto;
  overflow: hidden;
  box-shadow: 0 0 16px rgba(0, 0, 0, 0.3);
  position: relative;
  height: 588px;
  background-color: #fff;
}

.item-content {
  position: absolute;
  display: flex;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
}

.item-content--form {
  z-index: 10;
}

main.active .item-content--output-payment {
  z-index: 20;
}

.img-container {
  object-fit: cover;
  width: 50%;
  right: 0;
}

.content {
  background-color: white;
  padding: 16px 20px;
  width: 50%;
  left: 0;
}

.img-container,
.content {
  transition: 500ms ease-in-out;
  position: absolute;
  top: 0;
  height: 100%;
}

.title-form {
  color: #11161a;
  margin-bottom: 16px;
}

.wrap-input:not(:first-child) {
  margin-top: 1rem;
}

label {
  display: block;
  margin-bottom: 6px;
  font-size: 0.875rem;
  color: #11161a;
}

.input-form {
  width: 100%;
  border-radius: 4px;
  outline: none;
  padding: 6px;
  background-color: #e3e3e3;
  border: none;
}

.input-form:focus {
  box-shadow: 0 0 0 2px #566f83;
}

.input-form--disabled {
  cursor: not-allowed;
  background-color: #ccc;
}

.wrap-btn {
  display: flex;
  justify-content: center;
  gap: 14px;
  margin-top: 28px;
}

.btn {
  font-weight: 500;
  text-transform: uppercase;
  transition: 150ms ease-in;
  background-color: transparent;
  border: none;
  font-weight: 500;
  cursor: pointer;
}

.btn--send {
  background-color: #0d79d2;
  padding: 10px 24px;
  border-radius: 4px;
  color: #fff;
}

.btn--send:hover {
  background-color: #0f8ef5;
}

.btn--reset {
  color: rgb(165, 0, 0);
}

.btn--reset:hover {
  color: red;
}

.item-content--output-payment .content {
  top: 100%;
  right: 0;
  left: auto;
}

.item-content--output-payment .img-container {
  top: -100%;
  left: 0;
}

main.active .item-content--form .content {
  top: 100%;
}

main.active .item-content--form .img-container {
  top: -100%;
}

main.active .item-content--output-payment .img-container,
main.active .item-content--output-payment .content {
  top: 0;
}

main.active body {
  background-color: #567851;
}

/* Bagian konfirmasi detail */
.confirmation-detail > *:not(:first-child) {
  margin-top: 8px;
}

.container-description-output {
  display: flex;
  justify-content: space-between;
  gap: 20px;
  color: #11161a;
}

.description-output {
  width: 50%;
}

.value-output {
  display: block;
  width: 50%;
  font-weight: 600;
}

.wrap-btn--confirmation-detail {
  position: absolute;
  bottom: 16px;
  width: 100%;
}

.btn--edit {
  color: #0d79d2;
  text-decoration: underline;
}

.btn--edit:hover {
  color: #0f8ef5;
}

.btn--pay {
  background-color: rgb(17, 147, 48);
  padding: 10px 24px;
  border-radius: 4px;
  color: #fff;
}

.btn--pay:hover {
  background-color: rgb(16, 188, 56);
}

.city {
  text-transform: capitalize;
}

/* Popup confirmation */
.popup-confirmation {
  position: absolute;
  inset: 0;
  z-index: 40;
  background-color: rgba(0, 0, 0, 0.5);
  display: none;
  place-items: center;
}

.popup-confirmation.show,
.popup-check-detail-data.show {
  display: grid;
}

.subpopup-confirmation {
  background-color: #fff;
  padding: 20px;
  border-radius: 6px;
  color: #11161a;
}

.description-popup-confirmation {
  font-size: 20px;
  font-weight: 600;
}

.btn--no {
  text-decoration: underline;
}

.btn--no:hover {
  opacity: 0.8;
}

.btn--yes {
  background-color: rgb(17, 116, 43);
  color: #fff;
  border-radius: 4px;
  width: 104px;
  height: 48px;
}

.btn--yes:hover {
  background-color: rgb(24, 165, 62);
}

@keyframes loader {
  0% {
    transform: rotate(0);
  }

  100% {
    transform: rotate(360deg);
  }
}

.loader {
  animation: loader 1s linear infinite;
}

/* Pembelian tiket sukses */
.item-content--payment-success .content {
  top: 200%;
}

.item-content--payment-success .img-container {
  top: -200%;
}

main.success {
  background-color: #b6dffb;
}

main.success .item-content--payment-success {
  z-index: 40;
}

main.success .item-content--payment-success .content,
main.success .item-content--payment-success .img-container {
  top: 0;
}

main.success .item-content--form .content {
  top: 200%;
}

main.success .item-content--form .img-container {
  top: -200%;
}

.item-content--payment-success .content {
  display: grid;
  place-items: center;
  background-color: #1178bd;
  color: #fff;
  position: relative;
}

.item-content--payment-success .title-form {
  text-align: center;
  font-size: 28px;
  line-height: 48px;
  color: #fff;
}

.detail-data-payment {
  text-decoration: underline;
  text-align: center;
  cursor: pointer;
  position: absolute;
  left: 0;
  right: 0;
  bottom: 20px;
}

/* Popup check detail data */
.popup-check-detail-data {
  position: absolute;
  z-index: 40;
  background-color: rgba(0, 0, 0, 0.5);
  inset: 0;
  display: none;
  place-items: center;
}

.check-detail-data {
  background-color: #fff;
  border-radius: 6px;
  padding: 20px;
  position: relative;
  width: 500px;
}

.title-check-detail-data {
  color: #566f83;
  margin-bottom: 10px;
}

.close-detail-data {
  position: absolute;
  top: -10px;
  right: -10px;
  cursor: pointer;
}

.icon-success-payment {
  background: white;
  border-radius: 50%;
  margin: 0 auto 20px;
  display: block;
}

.popup {
  padding: 20px;
}

@media (max-width: 1120px) {
  .container {
    width: 520px;
  }

  .item-content .content {
    width: 100%;
    left: 0;
  }

  .img-container {
    display: none;
  }

  main.active .item-content--form .content {
    top: -100%;
  }

  main.success .item-content--form .content {
    top: -200%;
  }

  main.success .item-content--output-payment .content {
    top: -100%;
  }
}

@media (max-width: 576px) {
  main {
    padding: 10px 20px;
  }

  .container {
    width: 100%;
  }

  .container-description-output {
    font-size: 14px;
  }

  .subpopup {
    width: 100%;
  }
}

@media (max-width: 484px) {
  body {
    height: auto;
  }

  main {
    height: 100vh;
    position: relative;
    overflow: auto;
  }

  .container {
    height: 620px;
  }

  .confirmation-detail {
    height: 400px;
    overflow: auto;
  }

  .description-output,
  .value-output {
    width: auto;
  }

  .container-description-output {
    flex-direction: column;
    gap: 4px;
  }

  .detail-data-payment {
    font-size: 14px;
  }

  .item-content--payment-success .title-form {
    font-size: 24px;
  }

  .check-detail-data {
    height: 100%;
    overflow: auto;
  }

  .close-detail-data {
    top: 10px;
    right: 10px;
  }

  .container-description-output:not(.container-description-output:last-child) {
    margin-bottom: 10px;
  }
}
{% endcodeblock %}

Setelah kita menambahkan kode CSS diatas, maka tampilan halaman website kita sekarang akan menjadi seperti ini.
{% img /img/tutorial/revisi-program-pemesanan-tiket/css.png '"Tampilan CSS" "Tampilan CSS"' %}

Dan terakhir kita tambahkan javascript agar program kita bisa interaktif. Kamu bisa tuliskan kode javascript seperti ini.
{% codeblock script.js lang:javascript %}
const main = document.querySelector('main');
const formInput = document.querySelector('.item-content--form form');

// Ambil data-data yang telah diinputkan ketika user sudah submit
formInput.addEventListener('submit', function (e) {
  e.preventDefault();
  sendDataUser();
});

// Untuk melakukan validasi pada kota dituju dan jumlah orang
const totalPeople = document.getElementById('total-people');
const city = document.getElementById('city');

// Data semua kota yang dituju
const listCities = [...document.querySelectorAll('#list-city option')];

// Mengirim data-data yang telah diinputkan sekaligus memvalidasi nya
function sendDataUser() {
  const listCityToLowerCase = listCities.map((city) => {
    return city.value.toLowerCase();
  });
  const cityValueToLowerCase = city.value.toLowerCase();

  if (!listCityToLowerCase.includes(cityValueToLowerCase)) {
    city.value = '';
  } else if (totalPeople.value === '0') {
    totalPeople.value = '';
  } else {
    main.classList.add('active');
    getInputValueUser();
  }
}

// Kembali ke bagian form pembelian tiket, ketika user menekan bagian ubah
const btnEditPaymentTicket = document.querySelector('.btn--edit');
btnEditPaymentTicket.addEventListener('click', function () {
  main.classList.remove('active');
});

// Menerapkan kota-kota yang tersedia pada kota yang dituju
const discount = document.getElementById('discount');

for (const listCity of listCities) {
  city.addEventListener('change', function () {
    const cityValueToLowerCase = city.value.toLowerCase();
    const listCityToLowerCase = listCity.value.toLowerCase();

    if (cityValueToLowerCase === listCityToLowerCase) {
      const cityDiscount = listCity.dataset.discount || 0;
      discount.value = `${cityDiscount}%`;
    }
  });
}

// Mengambil data-data dari kolom input yang telah diisi oleh user
function getInputValueUser() {
  const name = document.getElementById('name').value;
  const status = document.getElementById('status').value;
  const paymentMethod = document.getElementById('payment-method').value;

  printInputValueUser(name, city.value, status, totalPeople.value, paymentMethod, discount.value);
}

function printInputValueUser(name, city, status, totalPeople, paymentMethod, discount) {
  const valueOutputs = [...document.querySelectorAll('.value-output')];

  const [outputName, outputCity, outputStatus, outputTotalPeople, outputPriceTicket, outputSubtotal, outputDiscount, outputTotalPayment, outputPaymentMethod] = valueOutputs;

  // Menampilkan nama user
  outputName.textContent = name;

  // Menampilkan kota yang dituju
  outputCity.textContent = city;

  // Menampilkan status apakah Dewasa atau Anak-anak
  outputStatus.textContent = status;

  // Menampilkan jumlah orang atau beli berapa tiket
  outputTotalPeople.textContent = totalPeople;

  // Menampilkan harga tiket sesuai dengan status yang diplih
  outputPriceTicket.textContent = `Rp ${outputStatus.textContent === 'Dewasa' ? '150.000' : '80.000'}`;

  // Melakukan perkalian pada subtotal
  const sumSubtotal = parseInt(outputPriceTicket.textContent.replace('Rp', '').split('.').join('') * outputTotalPeople.textContent);

  // Mengubah tanda koma menjadi titik
  outputSubtotal.textContent = `Rp ${sumSubtotal.toLocaleString().replaceAll(',', '.')}`;

  // Menampilkan diskon
  outputDiscount.textContent = discount;

  // Menghapu tanda persen pada diskon
  const removePercentOfDiscount = outputDiscount.textContent.replace('%', '');

  // Melakukan perhitungan apabila ada diskon
  const sumTotalPayment =
        removePercentOfDiscount === '0'
  ? outputSubtotal.textContent
  : `Rp ${parseInt((outputSubtotal.textContent.replace('Rp ', '').replaceAll('.', '') / 100) * (100 - removePercentOfDiscount))
  .toLocaleString()
  .replaceAll(',', '.')}`;

  // Menampilkan jumlah pembayaran
  outputTotalPayment.textContent = sumTotalPayment;

  // Menampilkan metode pembayaran yang dipilih
  outputPaymentMethod.textContent = paymentMethod;
}

// Popup konfirmasi
const popupConfirmation = document.querySelector('.popup-confirmation');
// popupConfirmation.addEventListener

// Ketika user membayar konfirmasi tiket
const btnPay = document.getElementById('btn-pay');
btnPay.addEventListener('click', function () {
  popupConfirmation.classList.add('show');
});

// Ketika user memilih tombol belum saat konfirmasi popup
const btnNoConfirmation = document.querySelector('.btn--no');
btnNoConfirmation.addEventListener('click', function () {
  popupConfirmation.classList.remove('show');
});

// Ketika user mengkonfirmasi bahwa detail data formulir tiket sudah benar dibagian popup konfirmasi
const btnConfirmation = document.querySelector('.btn--yes');
btnConfirmation.addEventListener('click', function () {
  // Mengubah text konfirmasi tiket data pembelian, menjadi mohon menunggu sebentar...
  const descriptionPopupConfirmation = document.querySelector('.description-popup-confirmation');
  descriptionPopupConfirmation.textContent = 'Mohon menunggu sebentar...';

  // Mengubah dari text sudah menjadi icon loading
  this.innerHTML = `
							<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24" class="loader">
								<path fill="none" d="M0 0h24v24H0z" />
								<path d="M18.364 5.636L16.95 7.05A7 7 0 1 0 19 12h2a9 9 0 1 1-2.636-6.364z" fill="rgba(255,255,255,1)" />
							</svg>
						`;

  // Menghilangkan tombol belum
  btnNoConfirmation.style.display = 'none';

  // Mengubah tampilan ketika semua transaksi sudah selesai

  // Memberikan sedikit efek loading sekitar 3detik
  setTimeout(() => {
    popupConfirmation.classList.remove('show');
    main.classList.replace('active', 'success');
  }, 3000);
});

// Menambahkan popup check detail data ketika text lihat detail data pembelian tiket di klik
const popupCheckDetailData = document.querySelector('.popup-check-detail-data');

const detailDataPayment = document.querySelector('.detail-data-payment');
detailDataPayment.addEventListener('click', function () {
  // Menambahkan popup check detail data
  popupCheckDetailData.classList.add('show');

  // Mengambil isi dari bagian konfirmasi data-data detail
  const confirmationDetail = document.querySelector('.item-content--output-payment .confirmation-detail');

  // Isi dari check detail data
  const checkDetailData = popupCheckDetailData.querySelector('.check-detail-data');

  // Mengubah bagian isi dari check detail data, menjadi data-data saat proses konfirmasi data pembelian tiket
  checkDetailData.innerHTML = `<h2 class="title-check-detail-data">Detail data:</h2>
					<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="36" height="36" class="close-detail-data">
						<path fill="none" d="M0 0h24v24H0z" />
						<path
							d="M12 22C6.477 22 2 17.523 2 12S6.477 2 12 2s10 4.477 10 10-4.477 10-10 10zm0-11.414L9.172 7.757 7.757 9.172 10.586 12l-2.829 2.828 1.415 1.415L12 13.414l2.828 2.829 1.415-1.415L13.414 12l2.829-2.828-1.415-1.415L12 10.586z"
							fill="rgba(255,61,61,1)"
						/>
					</svg>

					${confirmationDetail.innerHTML}`;

  closePopupDetail();
});

// Function untuk menghapus popup check detail data
function closePopupDetail() {
  const closePopupCheckDetail = document.querySelector('.close-detail-data');
  closePopupCheckDetail.addEventListener('click', function () {
    popupCheckDetailData.classList.remove('show');
  });
}
{% endcodeblock %}

Dan tadaaaa 🥳 website form pemesanan tiket kita sudah jadi. Kamu bisa uji coba buatan kamu, form pemesanan tiket ini hanya statis aja ya. Belum bisa menyimpan data-data ataupun benar-benar melakukan transaksi.

Jadi gimana? Apakah di kamu berjalan lancar sesuai dengan demo. Atau malah terjadi beberapa error atau bug. Jika ada kendala kamu bisa komentar atau chat saya di telegram ya.

Jadi cukup sekian aja tutorial mengenai revisi sederhana pada form pemesanan tiket kita. Demo nya kamu bisa cek di [Demo Revisi Form Pemesanan Tiket](http://form-pemesanan-tiket-revisi.surge.sh/).

Semoga bermanfaat gais
